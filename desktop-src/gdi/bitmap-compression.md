---
description: Windows supporta i formati per la compressione di bitmap che definiscono i colori con 8 o 4 bit per pixel. La compressione riduce l'archiviazione su disco e memoria necessaria per la bitmap.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Compressione bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3fa089401e77e882cf62472d007495e3e6c686d52259f095cb5a2758204736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105770"
---
# <a name="bitmap-compression"></a>Compressione bitmap

Windows supporta i formati per la compressione di bitmap che definiscono i colori con 8 o 4 bit per pixel. La compressione riduce l'archiviazione su disco e memoria necessaria per la bitmap.

Quando il **membro Compression** della struttura dell'intestazione delle informazioni bitmap è BI RLE8, viene usato un formato di codifica a lunghezza di esecuzione \_ (RLE) per comprimere una bitmap a 8 bit. Questo formato può essere compresso in modalità codificata o assoluta. Entrambe le modalità possono verificarsi in qualsiasi punto della stessa bitmap:

-   *La modalità* codificata è costituita da due byte: il primo byte specifica il numero di pixel consecutivi da disegnare usando l'indice dei colori contenuto nel secondo byte. Inoltre, il primo byte della coppia può essere impostato su zero per indicare un carattere di escape che indica la fine di una riga, la fine di una bitmap o un delta, a seconda del valore del secondo byte. L'interpretazione dell'escape dipende dal valore del secondo byte della coppia, che può essere uno dei valori seguenti.



| Valore | Significato                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Fine della riga.                                                                                                                                                |
| 1     | Fine della bitmap.                                                                                                                                              |
| 2     | Delta. I 2 byte successivi all'escape contengono valori senza segno che indicano gli offset orizzontale e verticale del pixel successivo dalla posizione corrente. |



 

-   In *modalità assoluta,* il primo byte è zero e il secondo byte è un valore compreso nell'intervallo compreso tra 03H e FFH. Il secondo byte rappresenta il numero di byte che seguono, ognuno dei quali contiene l'indice dei colori di un singolo pixel. Quando il secondo byte è minore o uguale a due, l'escape ha lo stesso significato della modalità codificata. In modalità assoluta, ogni esecuzione deve essere riempita con zero per terminare su un limite di parole a 16 bit.

L'esempio seguente mostra i valori esadecimali di una bitmap compressa a 8 bit:


```C++
[03 04] [05 06] [00 03 45 56 67 00] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



La bitmap si espande come indicato di seguito (i valori a due cifre rappresentano un indice dei colori per un singolo pixel):


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 down 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



Quando il **membro Compression** è BI RLE4, la bitmap viene compressa usando un formato di codifica di lunghezza di esecuzione per una bitmap a 4 bit, che usa anche le modalità codificate \_ e assolute:

-   In modalità codificata, il primo byte della coppia contiene il numero di pixel da disegnare usando gli indici dei colori nel secondo byte. Il secondo byte contiene due indici di colore, uno nei 4 bit più alti e uno nei 4 bit meno elevati. Il primo dei pixel viene disegnato usando il colore specificato dai 4 bit più alti, il secondo viene disegnato usando il colore nei 4 bit più bassi, il terzo viene disegnato usando il colore nei 4 bit più alti e così via, fino a quando non vengono disegnati tutti i pixel specificati dal primo byte.
-   In modalità assoluta, il primo byte è zero. Il secondo byte contiene il numero di indici di colore che seguono. I byte successivi contengono indici di colore nei relativi 4 bit alti e bassi, un indice di colore per ogni pixel. In modalità assoluta, ogni esecuzione deve essere allineata su un limite di parola. Le sequenze di escape end-of-line, end-of-bitmap e delta descritte per BI RLE8 si applicano anche alla compressione \_ BI \_ RLE4.

L'esempio seguente mostra i valori esadecimali di una bitmap compressa a 4 bit:


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



La bitmap si espande come indicato di seguito (i valori a cifra singola rappresentano un indice dei colori per un singolo pixel):


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 down 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



