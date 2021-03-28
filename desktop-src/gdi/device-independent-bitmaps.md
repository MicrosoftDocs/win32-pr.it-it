---
description: Una bitmap indipendente dal dispositivo (DIB) contiene una tabella dei colori.
ms.assetid: 56b39a3d-48a4-4620-9652-ec41ea4d6423
title: Bitmap Device-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aa35201a9a27c2d16a5a18b0125d25a3938890c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130799"
---
# <a name="device-independent-bitmaps"></a>Bitmap Device-Independent

Una bitmap indipendente dal dispositivo (DIB) contiene una *tabella dei colori*. Una tabella dei colori descrive il modo in cui i valori dei pixel corrispondono ai valori dei colori *RGB* , che descrivono i colori prodotti dalla creazione di una luce. Pertanto, una DIB può ottenere la combinazione di colori corretta su qualsiasi dispositivo. Una DIB contiene le informazioni relative al colore e alla dimensione seguenti:

-   Formato colori del dispositivo in cui è stata creata l'immagine rettangolare.
-   Risoluzione del dispositivo in cui è stata creata l'immagine rettangolare.
-   Tavolozza per il dispositivo in cui è stata creata l'immagine.
-   Matrice di bit che esegue il mapping dei tripletti rosso, verde, blu ( [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) ) ai pixel nell'immagine rettangolare.
-   Identificatore di compressione dei dati che indica lo schema di compressione dei dati, se presente, utilizzato per ridurre le dimensioni della matrice di bit.

Le informazioni relative al colore e alla dimensione vengono archiviate in una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , che è costituita da una struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) seguita da due o più strutture [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) . La struttura **BITMAPINFOHEADER** specifica le dimensioni del rettangolo pixel, descrive la tecnologia dei colori del dispositivo e identifica gli schemi di compressione utilizzati per ridurre le dimensioni della bitmap. Le strutture **RGBQUAD** identificano i colori visualizzati nel rettangolo pixel.

Sono disponibili due tipi di DIB:

-   Una DIB dal basso in alto, in cui l'origine si trova nell'angolo inferiore sinistro.
-   Una DIB dall'alto in basso, in cui l'origine si trova nell'angolo superiore sinistro.

Se l'altezza di una DIB, come indicato dal membro **Height** della struttura dell'intestazione delle informazioni bitmap, è un valore positivo, si tratta di una DIB dal basso in alto; Se l'altezza è un valore negativo, si tratta di una DIB dall'alto verso il basso. Non è possibile comprimere l'inizio dell'attività.

Il formato del colore viene specificato in termini di conteggio dei piani di colore e dei bit di colore. Il numero di piani di colore è sempre 1; il numero di bit di colore è 1 per le bitmap monocromatiche, 4 per le bitmap VGA e 8, 16, 24 o 32 per le bitmap in altri dispositivi a colori. Un'applicazione recupera il numero di bit di colore utilizzati da una particolare visualizzazione (o stampante) chiamando la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , specificando BITSPIXEL come secondo argomento.

La risoluzione di un dispositivo di visualizzazione viene specificata in pixel per contatore. Un'applicazione può recuperare la risoluzione orizzontale per uno schermo video, o stampante, seguendo questo processo in tre passaggi.

1.  Chiamare la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , specificando HORZRES come secondo argomento.
2.  Chiamare [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) una seconda volta, specificando HORZSIZE come secondo argomento.
3.  Dividere il primo valore restituito per il secondo valore restituito.

L'applicazione può recuperare la risoluzione verticale usando lo stesso processo in tre passaggi con parametri diversi: VERTRES al posto di HORZRES e VERTSIZE al posto di HORZSIZE.

La tavolozza è rappresentata da una matrice di strutture [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) che specificano i componenti di intensità rossa, verde e blu per ogni colore nella tavolozza dei colori di un dispositivo di visualizzazione. Ogni indice dei colori nella matrice della tavolozza è mappato a un pixel specifico nell'area rettangolare associata alla bitmap. La dimensione della matrice, in bit, equivale allo spessore del rettangolo, in pixel, moltiplicato per l'altezza del rettangolo, in pixel, moltiplicato per il numero di bit di colore per il dispositivo. Un'applicazione può recuperare le dimensioni della tavolozza del dispositivo chiamando la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , specificando NUMCOLORS come secondo argomento.

Windows supporta la compressione della matrice di tavolozze per la precedenza in base a 8 BPP e 4 BPP. Queste matrici possono essere compresse usando lo schema di codifica Run-Length (RLE). Lo schema RLE utilizza valori a 2 byte, il primo byte che specifica il numero di pixel consecutivi che utilizzano un indice dei colori e il secondo byte che specifica l'indice. Per ulteriori informazioni sulla compressione bitmap, vedere la descrizione delle strutture [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)e [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .

Un'applicazione può creare una DIB da un DDB inizializzando le strutture necessarie e chiamando la funzione [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) . Per determinare se un dispositivo supporta questa funzione, chiamare la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , specificando \_ \_ la bitmap RC di come flag RasterCaps.

Un'applicazione che deve copiare una bitmap può usare [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) per copiare tutti i pixel in una bitmap di origine in una bitmap di destinazione, ad eccezione dei pixel che corrispondono al colore trasparente.

Un'applicazione può usare una DIB per impostare i pixel sul dispositivo di visualizzazione chiamando la funzione [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) o [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) . Per determinare se un dispositivo supporta la funzione **SetDIBitsToDevice** , chiamare la funzione [**GETDEVICECAPS**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) specificando RC \_ DIBTODEV come flag RasterCaps. Specificare RC \_ STRETCHDIB come flag RasterCaps per determinare se il dispositivo supporta **StretchDIBits**.

Un'applicazione che deve semplicemente visualizzare una DIB preesistente può usare la funzione [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) . Ad esempio, un'applicazione per fogli di calcolo può aprire grafici esistenti e visualizzarli in una finestra usando la funzione **SetDIBitsToDevice** . Per ricreare ripetutamente una bitmap in una finestra, tuttavia, l'applicazione deve utilizzare la funzione [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) . Ad esempio, un'applicazione multimediale che combina grafica animata con un suono può trarre vantaggio dalla chiamata alla funzione **BitBlt** poiché viene eseguita più velocemente di **SetDIBitsToDevice**.

 

 
