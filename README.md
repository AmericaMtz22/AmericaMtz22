def analyze_text(file_path=None, text=None): 
    if text is None and file_path is not None:
        text = read_file(file_path)  # Leer desde archivo si no se proporciona el texto

    word_count, words = count_words(text)
    sentence_count = count_sentences(text)
    paragraph_count = count_paragraphs(text)
    avg_word_length = average_word_length(words)
    common_words = most_common_words(words)

    print(f"Cantidad de palabras: {word_count}")
    print(f"Cantidad de oraciones: {sentence_count}")
    print(f"Cantidad de párrafos: {paragraph_count}")
    print(f"Longitud promedio de palabras: {avg_word_length:.2f}")
    print(f"Palabras más comunes y sus frecuencias:")
    for word, freq in common_words:
        print(f"  {word}: {freq}")

# Llamar a la función con el texto directo
text = '''En un reino lejano, oculto entre las montañas más altas del mundo, vivía un dragón llamado Kaelar. A diferencia de otros de su especie, Kaelar no era temido por los habitantes del reino; en cambio, era su guardián. Cada noche, surcaba los cielos brillando con una luz dorada, pues tenía el poder de controlar las estrellas.

Los humanos le dejaban ofrendas en la cima de la montaña, pidiéndole protección. Pero Kaelar, en lo profundo de su corazón, anhelaba algo más que tesoros y oraciones. Quería conocer el calor de una amistad verdadera, pues su soledad era inmensa.

Un día, una niña llamada Lyra escaló la montaña para pedirle un deseo al dragón. No pidió riquezas ni poder, sino que Kaelar bajara de su montaña para ver las maravillas del mundo a su lado. Conmovido por su sinceridad, el dragón accedió. Juntos, Lyra y Kaelar viajaron a través de tierras mágicas, enfrentando desafíos y descubriendo que, a veces, el mayor tesoro es la compañía de alguien que te comprende.

Desde entonces, las noches brillaban aún más, pues Kaelar ya no cuidaba el reino solo, sino con su nueva amiga a su lado.'''
analyze_text(text=text)
M
