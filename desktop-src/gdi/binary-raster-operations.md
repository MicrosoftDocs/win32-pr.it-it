---
description: Questa sezione elenca i codici di operazione raster binari usati dalle funzioni GetROP2 e SetROP2. I codici di operazione raster definiscono il modo in cui GDI combina i bit della penna selezionata con i bit nella bitmap di destinazione.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Operazioni raster binarie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130855"
---
# <a name="binary-raster-operations"></a>Operazioni raster binarie

Questa sezione elenca i codici di operazione raster binari usati dalle funzioni [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) e [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) . I codici di operazione raster definiscono il modo in cui GDI combina i bit della penna selezionata con i bit nella bitmap di destinazione.

Ogni codice di operazione raster rappresenta un'operazione booleana in cui vengono combinati i valori dei pixel presenti nella penna selezionata e nella bitmap di destinazione. Di seguito sono riportati i due operandi utilizzati in queste operazioni.



| Operando | Significato            |
|---------|--------------------|
| P       | Penna selezionata       |
| D       | Bitmap di destinazione |



 

Gli operatori booleani utilizzati in queste operazioni seguono.



| Operatore | Significato                    |
|----------|----------------------------|
| a        | AND bit per bit                |
| n        | NOT bit per bit (inverso)      |
| o        | OR bit per bit                 |
| x        | OR esclusivo bit per bit (XOR) |



 

Tutte le operazioni booleane vengono presentate in notazione polacca inversa. Ad esempio, l'operazione seguente sostituisce i valori dei pixel nella bitmap di destinazione con una combinazione dei valori dei pixel della penna e del pennello selezionato:


```C++
DPo 
```



Ogni codice di operazione raster è un intero a 32 bit la cui parola più ordinata è un indice di operazione booleana e la cui parola di basso livello è il codice dell'operazione. L'indice dell'operazione a 16 bit è un valore a 8 bit esteso a zero che rappresenta tutti i possibili risultati risultante dall'operazione booleana su due parametri, in questo caso i valori di penna e di destinazione. Ad esempio, gli indici dell'operazione per le operazioni DPo e DPan sono illustrati nell'elenco seguente.



| P   | D   | DPo | Dpan |
|-----|-----|-----|------|
| 0   | 0   | 0   | 1    |
| 0   | 1   | 1   | 1    |
| 1   | 0   | 1   | 1    |
| 1   | 1   | 1   | 0    |



 

Nell'elenco seguente vengono descritte le modalità di disegno e le operazioni booleane che rappresentano.



| Operazione raster | Operazione booleana |
|------------------|-------------------|
| R2 \_ nero        | 0                 |
| \_COPYPEN R2      | P                 |
| \_MASKNOTPEN R2   | DPna              |
| \_MASKPEN R2      | DPa               |
| \_MASKPENNOT R2   | PDna              |
| \_MERGENOTPEN R2  | DPno              |
| \_MERGEPEN R2     | DPo               |
| \_MERGEPENNOT R2  | PDno              |
| \_NOP R2          | D                 |
| R2 \_ non          | Dn                |
| \_NOTCOPYPEN R2   | PN                |
| \_NOTMASKPEN R2   | DPan              |
| \_NOTMERGEPEN R2  | DPon              |
| \_NOTXORPEN R2    | DPxn              |
| \_Bianco R2        | 1                 |
| \_XORPEN R2       | DPx               |



 

Per un dispositivo monocromatico, GDI esegue il mapping tra il valore zero e il nero e il valore da 1 a bianco. Se un'applicazione tenta di creare con una penna nera in una destinazione bianca usando le operazioni raster binarie disponibili, si verificano i risultati seguenti.



| Operazione raster | Risultato             |
|------------------|--------------------|
| R2 \_ nero        | Linea nera visibile |
| \_COPYPEN R2      | Linea nera visibile |
| \_MASKNOTPEN R2   | Nessuna riga visibile    |
| \_MASKPEN R2      | Linea nera visibile |
| \_MASKPENNOT R2   | Linea nera visibile |
| \_MERGENOTPEN R2  | Nessuna riga visibile    |
| \_MERGEPEN R2     | Linea nera visibile |
| \_MERGEPENNOT R2  | Linea nera visibile |
| \_NOP R2          | Nessuna riga visibile    |
| R2 \_ non          | Linea nera visibile |
| \_NOTCOPYPEN R2   | Nessuna riga visibile    |
| \_NOTMASKPEN R2   | Nessuna riga visibile    |
| \_NOTMERGEPEN R2  | Linea nera visibile |
| \_NOTXORPEN R2    | Linea nera visibile |
| \_Bianco R2        | Nessuna riga visibile    |
| \_XORPEN R2       | Nessuna riga visibile    |



 

Per un dispositivo a colori, GDI USA valori RGB per rappresentare i colori della penna e della destinazione. Un valore di colore RGB è un valore long integer che contiene un campo di colore rosso, verde e blu, ognuno dei quali specifica l'intensità del colore specificato. Le intensità sono comprese tra 0 e 255. I valori vengono compressi nei tre byte di ordine inferiore del valore long integer. Il colore di una penna è sempre un colore a tinta unita, ma il colore della destinazione può essere costituito da una combinazione di due o tre colori. Se un'applicazione tenta di creare con una penna bianca in una destinazione blu usando le operazioni raster binarie disponibili, si verificano i risultati seguenti.



| Operazione raster | Risultato                 |
|------------------|------------------------|
| R2 \_ nero        | Linea nera visibile     |
| \_COPYPEN R2      | Riga bianca visibile     |
| \_MASKNOTPEN R2   | Linea nera visibile     |
| \_MASKPEN R2      | Linea blu invisibile    |
| \_MASKPENNOT R2   | Linea rossa/verde visibile |
| \_MERGENOTPEN R2  | Linea blu invisibile    |
| \_MERGEPEN R2     | Riga bianca visibile     |
| \_MERGEPENNOT R2  | Riga bianca visibile     |
| \_NOP R2          | Linea blu invisibile    |
| R2 \_ non          | Linea rossa/verde visibile |
| \_NOTCOPYPEN R2   | Linea nera visibile     |
| \_NOTMASKPEN R2   | Linea rossa/verde visibile |
| \_NOTMERGEPEN R2  | Linea nera visibile     |
| \_NOTXORPEN R2    | Linea blu invisibile    |
| \_Bianco R2        | Riga bianca visibile     |
| \_XORPEN R2       | Linea rossa/verde visibile |



 

 

 



