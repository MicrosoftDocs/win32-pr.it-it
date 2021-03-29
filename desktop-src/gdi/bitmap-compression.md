---
description: Windows supporta formati per la compressione di bitmap che definiscono i colori con 8 o 4 bit per pixel. La compressione riduce lo spazio di archiviazione su disco e memoria necessario per la bitmap.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Compressione bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38739f0e33f095b8eff567fc63b57db96b8cdc66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130854"
---
# <a name="bitmap-compression"></a>Compressione bitmap

Windows supporta formati per la compressione di bitmap che definiscono i colori con 8 o 4 bit per pixel. La compressione riduce lo spazio di archiviazione su disco e memoria necessario per la bitmap.

Quando il membro di **compressione** della struttura dell'intestazione delle informazioni bitmap è bi \_ RLE8, viene usato un formato di codifica RLE (Run-Length Encoding) per comprimere una bitmap a 8 bit. Questo formato può essere compresso in modalità codificata o Absolute. Entrambe le modalità possono essere presenti in qualsiasi punto della stessa bitmap:

-   La *modalità codificata* è costituita da due byte: il primo byte specifica il numero di pixel consecutivi da disegnare usando l'indice dei colori contenuto nel secondo byte. Inoltre, il primo byte della coppia può essere impostato su zero per indicare un carattere di escape che denota la fine di una riga, la fine di una bitmap o un Delta, a seconda del valore del secondo byte. L'interpretazione dell'escape dipende dal valore del secondo byte della coppia, che può essere uno dei valori seguenti.



| Valore | Significato                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Fine della riga.                                                                                                                                                |
| 1     | Fine della bitmap.                                                                                                                                              |
| 2     | Delta. I 2 byte che seguono l'escape contengono valori senza segno che indicano gli offset orizzontali e verticali del pixel successivo dalla posizione corrente. |



 

-   In *modalità Absolute* il primo byte è zero e il secondo byte è un valore compreso nell'intervallo da 03h a FFH. Il secondo byte rappresenta il numero di byte seguiti, ognuno dei quali contiene l'indice dei colori di un singolo pixel. Quando il secondo byte è due o meno, l'escape ha lo stesso significato della modalità codificata. In modalità Absolute ogni esecuzione deve essere allineata al confine di una parola.

Nell'esempio seguente vengono illustrati i valori esadecimali di una bitmap compressa a 8 bit:


```C++
[03 04] [05 06] [00 03 45 56 67] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



La bitmap si espande come segue (i valori a due cifre rappresentano un indice dei colori per un singolo pixel):


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



Quando il membro di **compressione** è bi \_ RLE4, la bitmap viene compressa usando un formato di codifica di lunghezza di esecuzione per una bitmap a 4 bit, che usa anche le modalità codificata e assoluta:

-   In modalità codificata, il primo byte della coppia contiene il numero di pixel da disegnare usando gli indici dei colori nel secondo byte. Il secondo byte contiene due indici di colore, uno nei 4 bit di ordine superiore e uno nei 4 bit di ordine inferiore. Il primo dei pixel viene disegnato usando il colore specificato dai 4 bit più significativi, il secondo viene disegnato usando il colore nei 4 bit di ordine inferiore, il terzo viene disegnato usando il colore nei 4 bit più significativi e così via, fino a quando non vengono disegnati tutti i pixel specificati dal primo byte.
-   In modalità Absolute il primo byte è zero. Il secondo byte contiene il numero di indici di colore che seguono. I byte successivi contengono indici di colore nei 4 bit di ordine superiore e inferiore, un indice dei colori per ogni pixel. In modalità Absolute ogni esecuzione deve essere allineata al confine di una parola. I caratteri di escape end-of-line, end-of-bitmap e Delta descritti per BI \_ RLE8 si applicano anche alla \_ compressione RLE4 di BI.

Nell'esempio seguente vengono illustrati i valori esadecimali di una bitmap compressa a 4 bit:


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



La bitmap si espande come segue (i valori a una sola cifra rappresentano un indice dei colori per un singolo pixel):


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



 

 



