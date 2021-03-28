---
description: È necessario salvare le bitmap in un file che usa il formato di file bitmap stabilito e assegnare un nome all'estensione bmp a tre caratteri.
ms.assetid: 44f19d14-4e0e-4512-8c86-6bd34ca4e87b
title: Archiviazione bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28046f6d78f5137d0dfc5b1396bbf76be318daa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130846"
---
# <a name="bitmap-storage"></a>Archiviazione bitmap

È necessario salvare le bitmap in un file che usa il formato di file bitmap stabilito e assegnare un nome all'estensione bmp a tre caratteri. Il formato del file bitmap stabilito è costituito da una struttura [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) seguita da una struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)o [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) . Una matrice di strutture [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) (detta anche tabella dei colori) segue la struttura dell'intestazione delle informazioni bitmap. La tabella dei colori è seguita da una seconda matrice di indici nella tabella dei colori (i dati effettivi della bitmap).

Il formato del file bitmap è illustrato nella figura seguente.

![diagramma del formato di file bitmap, che mostra la matrice BITMAPFILEHEADER, BITMAPINFOHEADER, RGBQUAD, e l'indice dei colori](images/csbmp-02.png)

I membri della struttura [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) identificano il file; specificare le dimensioni del file, in byte; e specificano l'offset dal primo byte nell'intestazione al primo byte dei dati bitmap. I membri della struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)o [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) specificano la larghezza e l'altezza della bitmap, in pixel; formato di colore (numero di piani di colore e bit di colore per pixel) del dispositivo di visualizzazione in cui è stata creata la bitmap; indica se i dati bitmap sono stati compressi prima dell'archiviazione e il tipo di compressione utilizzato. numero di byte di dati bitmap. risoluzione del dispositivo di visualizzazione in cui è stata creata la bitmap; e il numero di colori rappresentato nei dati. Le strutture [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) specificano i valori di intensità RGB per ognuno dei colori della tavolozza del dispositivo.

La matrice di indicizzazione dei colori associa un colore, sotto forma di indice a una struttura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , con ogni pixel in una bitmap. Il numero di bit nella matrice di indice dei colori corrisponde quindi al numero di pixel per il numero di bit necessari per indicizzare le strutture **RGBQUAD** . Ad esempio, una bitmap 8x8 Virtual nera e bianca ha una matrice di indice a colori di 8 \* 8 \* 1 = 64 bit, perché un bit è necessario per indicizzare due colori. La Redbrick.bmp, citata in [informazioni sulle bitmap](about-bitmaps.md), è una bitmap 32x32 con 16 colori; la matrice di indicizzazione del colore è 32 \* 32 \* 4 = 4096 bit perché a quattro bit a 16 colori.

Per creare una matrice di indice dei colori per una bitmap dall'alto verso il basso, iniziare dalla riga superiore della bitmap. L'indice di [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) per il colore del pixel più a sinistra è costituito dai primi *n* bit nell'array dei colori dell'indice (dove *n* è il numero di bit necessari per indicare tutte le strutture **RGBQUAD** ). Il colore del pixel successivo a destra corrisponde ai *n* bit successivi nella matrice e così via. Quando si raggiunge il pixel più a destra nella riga, continuare con il pixel più a sinistra nella riga seguente. Continua fino a quando non finisci con l'intera bitmap. Se si tratta di una bitmap dal basso verso l'alto, iniziare dalla riga inferiore della bitmap anziché dalla prima riga, ancora da sinistra verso destra e continuare fino alla riga superiore della bitmap.

Nell'output esadecimale seguente viene illustrato il contenuto del file Redbrick.bmp.


```C++
0000    42 4d 76 02 00 00 00 00  00 00 76 00 00 00 28 00 
0010    00 00 20 00 00 00 20 00  00 00 01 00 04 00 00 00 
0020    00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00 
0030    00 00 00 00 00 00 00 00  00 00 00 00 80 00 00 80 
0040    00 00 00 80 80 00 80 00  00 00 80 00 80 00 80 80 
0050    00 00 80 80 80 00 c0 c0  c0 00 00 00 ff 00 00 ff 
0060    00 00 00 ff ff 00 ff 00  00 00 ff 00 ff 00 ff ff 
0070    00 00 ff ff ff 00 00 00  00 00 00 00 00 00 00 00 
0080    00 00 00 00 00 00 00 00  00 00 00 00 00 00 09 00 
0090    00 00 00 00 00 00 11 11  01 19 11 01 10 10 09 09 
00a0    01 09 11 11 01 90 11 01  19 09 09 91 11 10 09 11 
00b0    09 11 19 10 90 11 19 01  19 19 10 10 11 10 09 01 
00c0    91 10 91 09 10 10 90 99  11 11 11 11 19 00 09 01 
00d0    91 01 01 19 00 99 11 10  11 91 99 11 09 90 09 91 
00e0    01 11 11 11 91 10 09 19  01 00 11 90 91 10 09 01 
00f0    11 99 10 01 11 11 91 11  11 19 10 11 99 10 09 10 
0100    01 11 11 11 19 10 11 09  09 10 19 10 10 10 09 01 
0110    11 19 00 01 10 19 10 11  11 01 99 01 11 90 09 19 
0120    11 91 11 91 01 11 19 10  99 00 01 19 09 10 09 19 
0130    10 91 11 01 11 11 91 01  91 19 11 00 99 90 09 01 
0140    01 99 19 01 91 10 19 91  91 09 11 99 11 10 09 91 
0150    11 10 11 91 99 10 90 11  01 11 11 19 11 90 09 11 
0160    00 19 10 11 01 11 99 99  99 99 99 99 99 99 09 99 
0170    99 99 99 99 99 99 00 00  00 00 00 00 00 00 00 00 
0180    00 00 00 00 00 00 90 00  00 00 00 00 00 00 00 00 
0190    00 00 00 00 00 00 99 11  11 11 19 10 19 19 11 09 
01a0    10 90 91 90 91 00 91 19  19 09 01 10 09 01 11 11 
01b0    91 11 11 11 10 00 91 11  01 19 10 11 10 01 01 11 
01c0    90 11 11 11 91 00 99 09  19 10 11 90 09 90 91 01 
01d0    19 09 91 11 01 00 90 10  19 11 00 11 11 00 10 11 
01e0    01 10 11 19 11 00 90 19  10 91 01 90 19 99 00 11 
01f0    91 01 11 01 91 00 99 09  09 01 10 11 91 01 10 91 
0200    99 11 10 90 91 00 91 11  00 10 11 01 10 19 19 09 
0210    10 00 99 01 01 00 91 01  19 91 19 91 11 09 10 11 
0220    00 91 00 10 90 00 99 01  11 10 09 10 10 19 09 01 
0230    91 90 11 09 11 00 90 99  11 11 11 90 19 01 19 01 
0240    91 01 01 19 09 00 91 10  11 91 99 09 09 90 11 91 
0250    01 19 11 11 91 00 91 19  01 00 11 00 91 10 11 01 
0260    11 11 10 01 11 00 99 99  99 99 99 99 99 99 99 99 
0270    99 99 99 99 99 90 
```



Nella tabella seguente vengono illustrati i byte di dati associati alle strutture in un file bitmap.



| Struttura                                    | Byte corrispondenti |
|----------------------------------------------|---------------------|
| [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) | 0x00 0x0D           |
| [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) | 0x35 0x0E           |
| Matrice [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)             | 0x36 0x75           |
| Matrice di indice colore                            | 0x76 0x275          |



 

 

 
