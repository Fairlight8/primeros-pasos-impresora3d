
# Calibración de los pasos del extrusor

## Explicación

Tu impresora 3D, durante el proceso de impresión, empuja filamento a través un bloque caliente y lo deposita en la cama o encima de las capas anteriores. La cuestión es **cuánto filamento deposita**. El slicer que uses (Cura, PrusaSlicer, etc.) lo calculará por ti en función de los parámetros que configures, como la altura de la capa. Sin embargo, para que la impresión sea precisa, debes calibrar tu extrusor para indicarle a la máquina la **correspondencia entre cuánto filamento debe empujar y cuánto empuja realmente**.

## Procedimiento

Para calibrar los pasos del extrusor, necesitas:

- Regla, calibre, cinta métrica, o algo para **medir**.
- Algo de papel o un rotulador. En resumen, algo para dejar una **marca** sobre el filamento.

Además, tendrás que controlar la impresora a través del ordenador con un programa como PronterFace. Si necesitas una guía para conectarla al ordenador, consulta primero la página **[Conectar la impresora al PC](conectar-pc.md)**. Hay varias formas de calibrar estos pasos. 

1. **Conecta la impresora al ordenador** a través del puerto serie, y abre el programa Pronterface (o el que uses).

2. **Mide 12 centímetros de filamento** desde la entrada/tope del extrusor, y marcarlos con cinta o con rotulador. Debes ser bastante preciso al medir, procura medir con el filamento recto.

3. Desde el PC, manda el comando 'G1 E100 F100'. Esta orden va a **empujar 10 centímetros de filamento**, a una velocidad bastante lenta. Mejor dicho, va a empujar lo que la impresora interpreta como 10 centímetros de filamento.

4. Ahora tienes que medir cuánto realmente ha empujado. Para ello, mide la **distancia** que todavía **queda desde la marca** de 12 centímetros hasta la entrada del extrusor. La distancia extruida realmente es de 12 - (distancia_restante).

5. La longitud de filamento extruida depende de los **pasos del extrusor**. Este es un índice que regular si el extrusor tiene que empujar más o menos. Para conocer los **E-steps** o pasos del extrusor ejecuta la orden 'M92' y busca la línea E-STEPS, en steps/mm. 

6. Ahora podemos hacer una **regla de tres**: Si con el valor de e-steps antiguo el extrusor empuja 12-distancia_restante, ¿cuánto debe valer para que empuje 10? La regla de tres es simple: (10 x e-steps_antiguos) / (12 - distancia_restante).

7. Por último, tienes que **introducir el nuevo valor** de pasos del extrusor con el comando 'M92 E___', metiendo el valor que has calculado después de la E. Si es un valor decimal, utiliza el punto para separar. Por ejemplo, 'M92 E46.1'. Para guardar los cambios, manda la orden 'M500'.



