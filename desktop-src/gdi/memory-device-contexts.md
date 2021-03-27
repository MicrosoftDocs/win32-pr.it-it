---
description: Per consentire alle applicazioni di inserire l'output in memoria anziché inviarlo a un dispositivo effettivo, usare un contesto di dispositivo speciale per le operazioni bitmap denominate un contesto di dispositivo di memoria.
ms.assetid: 0a682dc4-31a4-43c8-b0b1-ab01986b1dac
title: Contesti di dispositivo di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095de04fdf965a87011895015ad7ea6c9782e286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754383"
---
# <a name="memory-device-contexts"></a>Contesti di dispositivo di memoria

Per consentire alle applicazioni di inserire l'output in memoria anziché inviarlo a un dispositivo effettivo, usare un contesto di dispositivo speciale per le operazioni bitmap denominate un *contesto di dispositivo di memoria*. Un controller di dominio di memoria consente al sistema di considerare una parte della memoria come un dispositivo virtuale. Si tratta di una matrice di bit in memoria che un'applicazione può utilizzare temporaneamente per archiviare i dati relativi ai colori per le bitmap create in una superficie di disegno normale. Poiché la bitmap è compatibile con il dispositivo, anche un controller di dominio di memoria viene talvolta indicato come un *contesto di dispositivo compatibile*.

Il controller di dominio della memoria archivia le immagini bitmap per un dispositivo specifico. Un'applicazione può creare un controller di dominio di memoria chiamando la funzione [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) .

La bitmap originale in un controller di dominio di memoria è semplicemente un segnaposto. Le dimensioni sono un pixel di un pixel. Prima che un'applicazione possa iniziare a disegnare, deve selezionare una bitmap con la larghezza e l'altezza appropriate per il controller di dominio chiamando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Per creare una bitmap delle dimensioni appropriate, utilizzare la funzione [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)o [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) . Dopo aver selezionato la bitmap nel controller di dominio di memoria, il sistema sostituisce la matrice a bit singolo con una matrice sufficientemente grande da archiviare le informazioni sui colori per il rettangolo di pixel specificato.

Quando un'applicazione passa l'handle restituito da [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) a una delle funzioni di disegno, l'output richiesto non viene visualizzato nella superficie di disegno di un dispositivo. Al contrario, il sistema archivia le informazioni sui colori per la riga, la curva, il testo o l'area risultante nella matrice di bit. L'applicazione può copiare l'immagine archiviata in memoria in una superficie di disegno chiamando la funzione [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) , identificando il controller di dominio della memoria come contesto di dispositivo di origine e un controller di dominio della finestra o dello schermo come contesto di dispositivo di destinazione.

Quando si visualizza una DIB o un DDB creato da una DIB in un dispositivo tavolozza, è possibile migliorare la velocità con cui viene disegnata l'immagine organizzando la tavolozza logica in modo che corrisponda al layout della tavolozza di sistema. A tale scopo, chiamare [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) con il valore NUMRESERVED per ottenere il numero di colori riservati nel sistema. Chiamare quindi [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) e compilare la prima e l'ultima voce NUMRESERVED/2 della tavolozza logica con i colori di sistema corrispondenti. Se, ad esempio, NUMRESERVED è 20, inserire le prime e le ultime 10 voci della tavolozza logica con i colori di sistema. Inserire quindi i colori rimanenti 256-NUMRESERVED della tavolozza logica (in questo esempio, i restanti 236 colori) con i colori della DIB e impostare il \_ flag PC nocollapse su ognuno di questi colori.

Per ulteriori informazioni su colori e tavolozze, vedere [colori](colors.md). Per ulteriori informazioni sulle bitmap e sulle operazioni bitmap, vedere [bitmap](bitmaps.md).

 

 



