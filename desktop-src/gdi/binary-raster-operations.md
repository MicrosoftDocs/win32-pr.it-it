---
description: In questa sezione vengono elencati i codici di operazione raster binari usati dalle funzioni Get BINARY2 e SetUL2. I codici di operazione raster definiscono il modo in cui GDI combina i bit della penna selezionata con i bit nella bitmap di destinazione.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Operazioni raster binarie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462c07165d7f377f2a536722bf2f728446c308503108474cbb6a585cee6f68e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105810"
---
# <a name="binary-raster-operations"></a>Operazioni raster binarie

In questa sezione vengono elencati i codici di operazione raster binari usati dalle [**funzioni Get BINARY2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) [**e SetUL2.**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) I codici di operazione raster definiscono il modo in cui GDI combina i bit della penna selezionata con i bit nella bitmap di destinazione.

Ogni codice di operazione raster rappresenta un'operazione booleana in cui vengono combinati i valori dei pixel nella penna selezionata e nella bitmap di destinazione. Di seguito sono riportati i due operandi usati in queste operazioni.



| Operando | Significato            |
|---------|--------------------|
| P       | Penna selezionata       |
| D       | Bitmap di destinazione |



 

Seguono gli operatori booleani usati in queste operazioni.



| Operatore | Significato                    |
|----------|----------------------------|
| a        | AND bit per bit                |
| n        | NOT bit per bit (inverso)      |
| o        | OR bit per bit                 |
| x        | OR esclusivo bit per bit (XOR) |



 

Tutte le operazioni booleane vengono presentate in notazione polacco inversa. Ad esempio, l'operazione seguente sostituisce i valori dei pixel nella bitmap di destinazione con una combinazione dei valori in pixel della penna e del pennello selezionato:


```C++
DPo 
```



Ogni codice dell'operazione raster è un intero a 32 bit la cui parola più importante è un indice di operazione booleana e la cui parola meno importante è il codice dell'operazione. L'indice dell'operazione a 16 bit è un valore a 8 bit esteso zero che rappresenta tutti i possibili risultati risultanti dall'operazione booleana su due parametri (in questo caso, la penna e i valori di destinazione). Ad esempio, gli indici dell'operazione per le operazioni DPo e DPan sono visualizzati nell'elenco seguente.



| P   | D   | Dpo | Dpan |
|-----|-----|-----|------|
| 0   | 0   | 0   | 1    |
| 0   | 1   | 1   | 1    |
| 1   | 0   | 1   | 1    |
| 1   | 1   | 1   | 0    |



 

Nell'elenco seguente vengono descritte le modalità di disegno e le operazioni booleane che rappresentano.



| Operazione raster | Operazione booleana |
|------------------|-------------------|
| R2 \_ BLACK        | 0                 |
| R2 \_ COPYPEN      | P                 |
| R2 \_ MASKNOTPEN   | DPna              |
| R2 \_ MASKPEN      | Dpa               |
| R2 \_ MASKPENNOT   | PDna              |
| R2 \_ MERGENOTPEN  | DPno              |
| R2 \_ MERGEPEN     | Dpo               |
| R2 \_ MERGEPENNOT  | PDno              |
| R2 \_ NOP          | D                 |
| R2 \_ NOT          | Dn                |
| R2 \_ NOTCOPYPEN   | Pn                |
| R2 \_ NOTMASKPEN   | DPan              |
| R2 \_ NOTMERGEPEN  | DPon              |
| R2 \_ NOTXORPEN    | DPxn              |
| R2 \_ WHITE        | 1                 |
| R2 \_ XORPEN       | Dpx               |



 

Per un dispositivo monocromatico, GDI esegue il mapping del valore zero al nero e del valore 1 al bianco. Se un'applicazione tenta di disegnare con una penna nera su una destinazione bianca usando le operazioni raster binarie disponibili, si verificano i risultati seguenti.



| Operazione raster | Risultato             |
|------------------|--------------------|
| R2 \_ BLACK        | Linea nera visibile |
| R2 \_ COPYPEN      | Linea nera visibile |
| R2 \_ MASKNOTPEN   | Nessuna riga visibile    |
| R2 \_ MASKPEN      | Linea nera visibile |
| R2 \_ MASKPENNOT   | Linea nera visibile |
| R2 \_ MERGENOTPEN  | Nessuna riga visibile    |
| R2 \_ MERGEPEN     | Linea nera visibile |
| R2 \_ MERGEPENNOT  | Linea nera visibile |
| R2 \_ NOP          | Nessuna riga visibile    |
| R2 \_ NOT          | Linea nera visibile |
| R2 \_ NOTCOPYPEN   | Nessuna riga visibile    |
| R2 \_ NOTMASKPEN   | Nessuna riga visibile    |
| R2 \_ NOTMERGEPEN  | Linea nera visibile |
| R2 \_ NOTXORPEN    | Linea nera visibile |
| R2 \_ WHITE        | Nessuna riga visibile    |
| R2 \_ XORPEN       | Nessuna riga visibile    |



 

Per un dispositivo a colori, GDI usa valori RGB per rappresentare i colori della penna e della destinazione. Un valore di colore RGB è un long integer che contiene un campo di colore rosso, verde e blu, ognuno dei quali specifica l'intensità del colore specificato. Le intensità sono da 0 a 255. I valori sono compressi nei tre byte di ordine più basso del long integer. Il colore di una penna è sempre a tinta unita, ma il colore della destinazione può essere una combinazione di due o tre colori qualsiasi. Se un'applicazione tenta di disegnare con una penna bianca su una destinazione blu usando le operazioni raster binarie disponibili, si verificano i risultati seguenti.



| Operazione raster | Risultato                 |
|------------------|------------------------|
| R2 \_ BLACK        | Linea nera visibile     |
| R2 \_ COPYPEN      | Riga bianca visibile     |
| MASCHERA \_ R2NOTPEN   | Linea nera visibile     |
| R2 \_ MASKPEN      | Linea blu invisibile    |
| R2 \_ MASKPENNOT   | Linea rossa/verde visibile |
| R2 \_ MERGENOTPEN  | Linea blu invisibile    |
| R2 \_ MERGEPEN     | Riga bianca visibile     |
| R2 \_ MERGEPENNOT  | Riga bianca visibile     |
| R2 \_ NOP          | Linea blu invisibile    |
| R2 \_ NOT          | Linea rossa/verde visibile |
| R2 \_ NOTCOPYPEN   | Linea nera visibile     |
| R2 \_ NOTMASKPEN   | Linea rossa/verde visibile |
| R2 \_ NOTMERGEPEN  | Linea nera visibile     |
| R2 \_ NOTXORPEN    | Linea blu invisibile    |
| R2 \_ WHITE        | Riga bianca visibile     |
| R2 \_ XORPEN       | Linea rossa/verde visibile |



 

 

 



