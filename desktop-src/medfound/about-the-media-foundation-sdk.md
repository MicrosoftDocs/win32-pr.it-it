---
description: Microsoft Media Foundation è la piattaforma multimediale di nuova generazione per Windows che consente a sviluppatori, consumer e provider di contenuti di adottare la nuova generazione di contenuti Premium con affidabilità avanzata, qualità senza precedenti e interoperabilità senza precedenti.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: Informazioni su Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2f8510cc6d967f7a3a809d395f032e277290074002399f9b54e6c54025c312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959651"
---
# <a name="about-media-foundation"></a>Informazioni su Media Foundation

Microsoft Media Foundation è la piattaforma multimediale di nuova generazione per Windows che consente a sviluppatori, consumer e provider di contenuti di adottare la nuova generazione di contenuti Premium con affidabilità avanzata, qualità senza precedenti e interoperabilità senza precedenti.

Media Foundation richiede Windows Vista o versione successiva. Usa il modello a oggetti del componente (COM) e richiede C/C++. Microsoft non fornisce un'API gestita per Media Foundation.

Le API Media Foundation sono parte di [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Per sviluppare un'Media Foundation, installare la versione più recente di Windows SDK.

## <a name="audio-and-video-quality"></a>Qualità audio e video

Media Foundation è stato progettato per soddisfare le sfide poste dal contenuto ad alta definizione. I miglioramenti apportati alla qualità audio e video in tutta la piattaforma ora rendono possibile offrire un'esperienza ottimale per i contenuti ad alta definizione di prossima generazione.

-   DirectX Video Acceleration (DXVA) 2.0 offre un'accelerazione video più efficiente rispetto a DXVA 1.0, con decodifica video più affidabile e semplificata e uso esteso dell'hardware nell'elaborazione video. Con DXVA 2.0, Windows può gestire alcuni dei contenuti ad alta definizione più impegnativi con alta qualità e resilienza migliorata.

-   Le informazioni sullo spazio colore vengono mantenute in tutta la pipeline video. Gli utenti possono usufruire di contenuti video con la massima fedeltà. Le informazioni sui colori e le immagini interlacciate vengono ora passate all'hardware per le composizione a passaggio singolo. Il mantenimento delle informazioni sullo spazio colore riduce anche le conversioni non necessarie dello spazio colore, che libera più cicli per elaborare contenuti HD impegnativi.
-   Il renderer video avanzato (EVR) offre un migliore supporto per la temporizzazione, un'elaborazione video migliorata e una migliore resilienza degli glitch. Il supporto per la riproduzione a schermo intero è stato migliorato e la rimozione di video in modalità finestra è stata ridotta a icona.
-   Media Foundation usa il servizio Utilità di pianificazione classi multimediali (MMCSS), un nuovo servizio di sistema in Windows Vista. MMCSS consente alle applicazioni multimediali di garantire che l'elaborazione a tempo limitato riceva l'accesso in ordine di priorità alle risorse della CPU.

## <a name="content-access"></a>Accesso al contenuto

Quando l'intrattenimento digitale passa all'era ad alta definizione e il contenuto diventa più portabile e onniquitoso, la protezione del contenuto diventerà parte integrante dei prodotti multimediali digitali. L'estendibilità Media Foundation garantisce che sia in grado di supportare queste tendenze.

Inoltre, l Media Foundation estendibilità consente a diversi sistemi di protezione del contenuto di operare insieme.

## <a name="about-media-foundation"></a>Informazioni su Media Foundation

Questa sezione contiene informazioni generali sulle MEDIA FOUNDATION seguenti. Informazioni dettagliate sulla programmazione sono disponibili nella guida [Media Foundation programmazione.](media-foundation-programming-guide.md)



| Sezione                                                                              | Descrizione                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Novità di Media Foundation](whats-new-for-media-foundation.md)                | Vengono descritte le nuove funzionalità di Media Foundation.                               |
| [Media Foundation intestazioni e librerie](media-foundation-headers-and-libraries.md) | Elenca i file di intestazione e di libreria che definiscono Media Foundation API. |
| [strumenti Media Foundation](media-foundation-tools.md)                                 | Vengono descritti gli strumenti di sviluppo disponibili per Media Foundation.  |



 

Media Foundation non è incluso nelle edizioni N e ENTERPRISE di Windows 8. Per altre informazioni, vedere Microsoft Windows Media Feature Pack per le versioni N e [ENTERPRISE di tutte le Windows 8 edizioni.](https://support.microsoft.com/kb/2703761)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



