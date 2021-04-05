---
title: Informazioni sulle funzioni DrawDib
description: Informazioni sulle funzioni DrawDib
ms.assetid: 0ae993df-8393-479e-aa11-14301384715d
keywords:
- Video per Windows (VFW), DrawDib
- VFW (video per Windows), DrawDib
- DrawDib, informazioni
- DrawDib, tabelle colori
- DrawDib, modalità di trasferimento
- DrawDib, schede di visualizzazione
- DrawDib, estensione dell'immagine
- DrawDib, immagini compresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f3e9ba822e16a7568775378b24f69bbca12de
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726306"
---
# <a name="about-the-drawdib-functions"></a>Informazioni sulle funzioni DrawDib

Collettivamente, le funzioni DrawDib sono simili alla funzione [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) in quanto forniscono funzionalità di estensione dell'immagine e dithering. Tuttavia, le funzioni DrawDib supportano la decompressione delle immagini, il flusso di dati e un numero maggiore di schede di visualizzazione.

In alcune circostanze, è utile utilizzare le funzioni DrawDib. Tuttavia, [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) è più vario delle funzioni DrawDib e deve essere usato quando le funzioni DrawDib non possono fornire la funzionalità desiderata. Nell'elenco seguente vengono descritti i fattori da considerare quando si decide se utilizzare le funzioni DrawDib o **StretchDIBits**.

-   Formato informazioni tabella colori. Le funzioni DrawDib visualizzano immagini che usano il formato **\_ \_ colori RGB DIB** per la tabella dei colori. Se le immagini nell'applicazione archiviano informazioni sulla tabella dei colori con il formato **DIB \_ PAL \_ Colors** o **DIB \_ PAL \_ indicis** , è necessario usare [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) per visualizzarle.
-   Modalità di trasferimento. Per le funzioni DrawDib è necessario che l'applicazione usi la modalità di trasferimento **SRCCOPY** . Se l'applicazione usa [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) con una modalità di trasferimento diversa da **SRCCOPY**, è necessario continuare a usare **StretchDIBits**. Analogamente, se è necessario usare altre operazioni raster nell'applicazione, ad esempio XOR, usare **StretchDIBits**.
-   Qualità della riproduzione video e animazione. È possibile usare le funzioni DrawDib per le applicazioni di streaming di dati, ad esempio quelle che riproducono clip video e sequenze animate. Le funzioni DrawDib superano [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) in quanto forniscono immagini di qualità superiore e migliorano il movimento durante la riproduzione.
-   Schede di visualizzazione. Le funzioni DrawDib supportano un numero maggiore di schede di visualizzazione rispetto a quelle supportate da [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) . Le funzioni DrawDib supportano le schede dei colori VGA che forniscono tavolozze a 16 colori con profondità dell'immagine a 4 bit, adattatori SVGA che forniscono tavolozze dei colori 256 con profondità dell'immagine a 8 bit e adattatori di visualizzazione a colori reali che forniscono migliaia di colori con profondità delle immagini a 16 bit, a 24 bit e a 32 bit.

    Le funzioni DrawDib migliorano anche la velocità e la qualità della visualizzazione delle immagini in schede video con funzionalità più limitate. Ad esempio, quando si usa una scheda di visualizzazione a 8 bit, DrawDib funziona in modo efficiente dithering di immagini con colori reali a 256 colori. Dithering anche immagini a 8 bit quando si usano schede di visualizzazione a 4 bit.

-   Estensione dell'immagine. Analogamente a [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits), le funzioni DrawDib utilizzano i rettangoli di origine e di destinazione per controllare la parte di un'immagine visualizzata. È possibile ritagliare parti indesiderate di un'immagine o allungare un'immagine variando la posizione e le dimensioni dei rettangoli di origine e di destinazione. Se un driver video non supporta l'estensione delle immagini, le funzioni DrawDib forniscono funzionalità di estensione più efficienti rispetto a **StretchDIBits**.
-   Immagini compresse. Le funzioni DrawDib determineranno qualsiasi formato per il quale si dispone di un decompressore, tra cui la codifica Run-Length (RLE), Cinepak e 411 YUV. Windows include i decompressori RLE e Cinepak che possono essere installati facoltativamente.
-   Il codec Indeo non è più supportato in Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DrawDib](drawdib.md)
</dt> </dl>

 

 