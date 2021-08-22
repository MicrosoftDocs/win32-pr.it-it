---
title: Informazioni sulle funzioni DrawDib
description: Informazioni sulle funzioni DrawDib
ms.assetid: 0ae993df-8393-479e-aa11-14301384715d
keywords:
- Video per Windows (VFW),DrawDib
- VFW (Video per Windows),DrawDib
- DrawDib,about
- DrawDib, tabelle dei colori
- DrawDib, modalità di trasferimento
- DrawDib, adattatori di visualizzazione
- DrawDib, estensione delle immagini
- DrawDib, immagini compresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e03b41d5af776c39f7d100e9478bd408011d61d8e3d661cb80bd9ab52f08c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942089"
---
# <a name="about-the-drawdib-functions"></a>Informazioni sulle funzioni DrawDib

Collettivamente, le funzioni DrawDib sono simili alla funzione [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) in quanto forniscono funzionalità di estensione e dithering delle immagini. Tuttavia, le funzioni DrawDib supportano la decompressione di immagini, lo streaming dei dati e un numero maggiore di schede di visualizzazione.

In alcune circostanze può risultare utile usare le funzioni DrawDib. [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) è comunque più diversificato rispetto alle funzioni DrawDib e deve essere usato quando le funzioni DrawDib non possono fornire la funzionalità desiderata. L'elenco seguente descrive i fattori da considerare quando si decide se usare le funzioni DrawDib o **StretchDIBits.**

-   Formato delle informazioni sulla tabella dei colori. Le funzioni DrawDib visualizzano immagini che usano il **formato COLORI \_ RGB \_ DIB** per la tabella dei colori. Se le immagini nell'applicazione archiviano informazioni sulla tabella dei colori con il formato **DIB \_ PAL \_ COLORS** o **DIB \_ PAL \_ INDICES,** è necessario usare [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) per visualizzarle.
-   Modalità di trasferimento. Le funzioni DrawDib richiedono che l'applicazione usi **la modalità di trasferimento SRCCOPY.** Se l'applicazione [**usa StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) con una modalità di trasferimento diversa da **SRCCOPY,** è consigliabile continuare a usare **StretchDIBits.** Analogamente, se è necessario usare altre operazioni raster nell'applicazione, ad esempio XOR, usare **StretchDIBits.**
-   Qualità della riproduzione di video e animazioni. È possibile usare le funzioni DrawDib per le applicazioni di streaming dei dati, ad esempio quelle che riproducino clip video e sequenze animate. Le funzioni DrawDib offrono prestazioni migliori rispetto a [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) in quanto forniscono immagini di qualità superiore e migliorano il movimento durante la riproduzione.
-   Adattatori di visualizzazione. Le funzioni DrawDib supportano un numero maggiore di schede di visualizzazione rispetto a quelle supportate da [**StretchDIBits.**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) Le funzioni DrawDib supportano schede colori VGA che forniscono tavolozze a 16 colori che usano la profondità dell'immagine a 4 bit, schede SVGA che forniscono tavolozze a 256 colori con profondità dell'immagine a 8 bit e schede di visualizzazione a colori reale che forniscono migliaia di colori con intensità di immagini a 16 bit, a 24 bit e a 32 bit.

    Le funzioni DrawDib migliorano anche la velocità e la qualità della visualizzazione delle immagini nelle schede video con funzionalità più limitate. Ad esempio, quando si usa una scheda di visualizzazione a 8 bit, drawDib esegue in modo efficiente il dithering delle immagini di colore reale a 256 colori. Vengono inoltre dithering di immagini a 8 bit quando si usano schede di visualizzazione a 4 bit.

-   Estensione delle immagini. Come [**StretchDIBits,**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)le funzioni DrawDib usano rettangoli di origine e di destinazione per controllare la parte di un'immagine visualizzata. È possibile ritagliare parti indesiderate di un'immagine o estendere un'immagine variando la posizione e le dimensioni dei rettangoli di origine e di destinazione. Se un driver video non supporta l'estensione delle immagini, le funzioni DrawDib offrono funzionalità di estensione più efficienti rispetto a **StretchDIBits.**
-   Immagini compresse. Le funzioni DrawDib disegnano qualsiasi formato per cui si dispone di un decompressore, tra cui la codifica a lunghezza di esecuzione (RLE), Cinepak e 411 YUV. Windows include decompressori RLE e Cinepak che possono essere installati facoltativamente.
-   Il codec Indeo non è più supportato in Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DrawDib](drawdib.md)
</dt> </dl>

 

 