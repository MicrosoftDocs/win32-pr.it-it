---
description: Per consentire alle applicazioni di inserire l'output in memoria anziché inviarlo a un dispositivo effettivo, usare un contesto di dispositivo speciale per le operazioni bitmap denominate contesto di dispositivo di memoria.
ms.assetid: 0a682dc4-31a4-43c8-b0b1-ab01986b1dac
title: Contesti di dispositivo di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63469823e38eb98da5d43ede006e6b1e64af874d300127db6cd4cc7743672d29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760059"
---
# <a name="memory-device-contexts"></a>Contesti di dispositivo di memoria

Per consentire alle applicazioni di inserire l'output in memoria anziché inviarlo a un dispositivo effettivo, usare un contesto di dispositivo speciale per le operazioni bitmap denominato contesto *di dispositivo di memoria*. Un controller di dominio di memoria consente al sistema di considerare una parte di memoria come dispositivo virtuale. Si tratta di una matrice di bit in memoria che un'applicazione può usare temporaneamente per archiviare i dati sui colori per le bitmap create su una normale superficie di disegno. Poiché la bitmap è compatibile con il dispositivo, un controller di dominio di memoria viene talvolta definito anche contesto *di dispositivo compatibile.*

Il controller di dominio di memoria archivia le immagini bitmap per un dispositivo specifico. Un'applicazione può creare un controller di dominio di memoria chiamando la [**funzione CreateCompatibleDC.**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)

La bitmap originale in un controller di dominio di memoria è semplicemente un segnaposto. Le dimensioni sono di un pixel per pixel. Prima di iniziare a disegnare, un'applicazione deve selezionare una bitmap con la larghezza e l'altezza appropriate nel controller di dominio chiamando la [**funzione SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Per creare una bitmap delle dimensioni appropriate, usare la [**funzione CreateBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)o [**CreateCompatibleBitmap.**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) Dopo aver selezionato la bitmap nel controller di dominio di memoria, il sistema sostituisce la matrice a bit singolo con una matrice sufficientemente grande da archiviare le informazioni sul colore per il rettangolo di pixel specificato.

Quando un'applicazione passa l'handle restituito da [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) a una delle funzioni di disegno, l'output richiesto non viene visualizzato sull'area di disegno di un dispositivo. Il sistema archivia invece le informazioni sul colore per la linea, la curva, il testo o l'area risultante nella matrice di bit. L'applicazione può copiare l'immagine archiviata in memoria su una superficie di disegno chiamando la funzione [**BitBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) identificando il controller di dominio di memoria come contesto di dispositivo di origine e un controller di dominio finestra o schermo come contesto di dispositivo di destinazione.

Quando si visualizza un file DIB o un DDB creato da un dib in un dispositivo tavolozza, è possibile migliorare la velocità con cui viene disegnata l'immagine disponendo la tavolozza logica in modo che corrisponda al layout del riquadro di sistema. A tale scopo, chiamare [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) con il valore NUMRESERVED per ottenere il numero di colori riservati nel sistema. Chiamare quindi [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) e compilare la prima e l'ultima voce NUMRESERVED/2 della tavolozza logica con i colori di sistema corrispondenti. Ad esempio, se NUMRESERVED è 20, è necessario compilare la prima e le ultime 10 voci della tavolozza logica con i colori di sistema. Compilare quindi i restanti 256 colori NUMRESERVED della tavolozza logica (in questo esempio, i restanti 236 colori) con i colori della dib e impostare il flag NOCOLLAPSE del PC su ognuno di \_ questi colori.

Per altre informazioni sui colori e le tavolozze, vedere [Colori](colors.md). Per altre informazioni sulle bitmap e sulle operazioni bitmap, vedere [Bitmap .](bitmaps.md)

 

 



