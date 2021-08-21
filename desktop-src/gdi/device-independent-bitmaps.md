---
description: Una bitmap indipendente dal dispositivo (DIB) contiene una tabella dei colori.
ms.assetid: 56b39a3d-48a4-4620-9652-ec41ea4d6423
title: Device-Independent bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6672857aadda714e7016616ca78654d7da102b48c1229c5b322953fc716f5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761390"
---
# <a name="device-independent-bitmaps"></a>Device-Independent bitmap

Una bitmap indipendente dal dispositivo (DIB) contiene una *tabella dei colori*. Una tabella dei colori descrive il modo in cui i valori dei pixel corrispondono ai *valori di colore RGB,* che descrivono i colori prodotti dall'emissione di luce. Di conseguenza, un DIB può ottenere la combinazione di colori appropriata in qualsiasi dispositivo. Un dib contiene le informazioni sul colore e sulle dimensioni seguenti:

-   Formato del colore del dispositivo in cui è stata creata l'immagine rettangolare.
-   Risoluzione del dispositivo in cui è stata creata l'immagine rettangolare.
-   Riquadro per il dispositivo in cui è stata creata l'immagine.
-   Matrice di bit che esegue il mapping delle triple rosse, verdi, blu ( [**RGB)**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) ai pixel nell'immagine rettangolare.
-   Identificatore di compressione dati che indica lo schema di compressione dei dati (se presente) usato per ridurre le dimensioni della matrice di bit.

Le informazioni sul colore e sulla dimensione vengono archiviate in una struttura [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) costituita da una [**struttura BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) seguita da due o più [**strutture RGBQUAD.**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) La **struttura BITMAPINFOHEADER** specifica le dimensioni del rettangolo in pixel, descrive la tecnologia dei colori del dispositivo e identifica gli schemi di compressione usati per ridurre le dimensioni della bitmap. Le **strutture RGBQUAD** identificano i colori visualizzati nel rettangolo in pixel.

Esistono due tipi di DIB:

-   DIB in basso verso l'alto, in cui l'origine si trova nell'angolo inferiore sinistro.
-   DIB dall'alto verso il basso, in cui l'origine si trova nell'angolo superiore sinistro.

Se l'altezza di un DIB, come indicato dal membro **Height** della struttura dell'intestazione delle informazioni bitmap, è un valore positivo, si tratta di un DIB in basso verso l'alto. se l'altezza è un valore negativo, è un DIB dall'alto verso il basso. I DIB dall'alto verso il basso non possono essere compressi.

Il formato del colore viene specificato in termini di conteggio dei piani colori e dei bit di colore. Il conteggio dei piani colore è sempre 1; il numero di bit di colore è 1 per le bitmap monocroma, 4 per le bitmap VGA e 8, 16, 24 o 32 per le bitmap in altri dispositivi a colori. Un'applicazione recupera il numero di bit di colore utilizzati da una determinata visualizzazione (o stampante) chiamando la [**funzione GetDeviceCaps,**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) specificando BITSPIXEL come secondo argomento.

La risoluzione di un dispositivo di visualizzazione è specificata in pixel per metro. Un'applicazione può recuperare la risoluzione orizzontale per uno schermo video o una stampante seguendo questo processo in tre passaggi.

1.  Chiamare la [**funzione GetDeviceCaps,**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) specificando HORZRES come secondo argomento.
2.  Chiamare [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) una seconda volta, specificando HORZSIZE come secondo argomento.
3.  Dividere il primo valore restituito per il secondo valore restituito.

L'applicazione può recuperare la risoluzione verticale usando lo stesso processo in tre passaggi con parametri diversi: VERTRES al posto di HORZRES e VERTSIZE al posto di HORZSIZE.

La tavolozza è rappresentata da una matrice di [**strutture RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) che specificano i componenti di intensità rosso, verde e blu per ogni colore nella tavolozza dei colori di un dispositivo di visualizzazione. Ogni indice colori nella matrice della tavolozza viene mappato a un pixel specifico nell'area rettangolare associata alla bitmap. Le dimensioni di questa matrice, in bit, sono equivalenti alla larghezza del rettangolo, in pixel, moltiplicata per l'altezza del rettangolo, in pixel, moltiplicata per il numero di bit di colore per il dispositivo. Un'applicazione può recuperare le dimensioni della tavolozza del dispositivo chiamando la [**funzione GetDeviceCaps,**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) specificando NUMCOLORS come secondo argomento.

Windows supporta la compressione della matrice di palette per DIB bottom-up a 8 bpp e 4 bpp. Queste matrici possono essere compresse usando lo schema di codifica della lunghezza di esecuzione (RLE). Lo schema RLE usa valori a 2 byte, il primo byte che specifica il numero di pixel consecutivi che usano un indice colori e il secondo byte che specifica l'indice. Per altre informazioni sulla compressione bitmap, vedere la descrizione delle strutture [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)e [**BITMAPV5HEADER.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

Un'applicazione può creare un DIB da un database DDB inizializzando le strutture necessarie e chiamando la [**funzione GetDIBits.**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) Per determinare se un dispositivo supporta questa funzione, chiamare la [**funzione GetDeviceCaps,**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) specificando RC \_ DI BITMAP come flag \_ RASTERCAPS.

Un'applicazione che deve copiare una bitmap può usare [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) per copiare tutti i pixel di una bitmap di origine in una bitmap di destinazione, ad eccezione dei pixel che corrispondono al colore trasparente.

Un'applicazione può usare un DIB per impostare i pixel sul dispositivo di visualizzazione chiamando la [**funzione SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) o [**StretchDIBits.**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) Per determinare se un dispositivo supporta la **funzione SetDIBitsToDevice,** chiamare la [**funzione GetDeviceCaps,**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) specificando RC \_ DIBTODEV come flag RASTERCAPS. Specificare RC STRETCHDIB come flag RASTERCAPS per determinare se il \_ dispositivo supporta **StretchDIBits.**

Un'applicazione che deve semplicemente visualizzare un DIB preesiste può usare la [**funzione SetDIBitsToDevice.**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) Ad esempio, un'applicazione foglio di calcolo può aprire grafici esistenti e visualizzarli in una finestra usando la **funzione SetDIBitsToDevice.** Per ridisegnare ripetutamente una bitmap in una finestra, tuttavia, l'applicazione deve usare la [**funzione BitBlt.**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) Ad esempio, un'applicazione multimediale che combina grafica animata con audio trarrebbe vantaggio dalla chiamata alla funzione **BitBlt** perché viene eseguita più velocemente rispetto a **SetDIBitsToDevice.**

 

 
