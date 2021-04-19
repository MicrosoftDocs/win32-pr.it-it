---
description: Microsoft Media Foundation è la piattaforma multimediale di nuova generazione per Windows che consente a sviluppatori, consumer e provider di contenuti di adottare la nuova onda di contenuti Premium con affidabilità avanzata, qualità impareggiabile e interoperabilità senza problemi.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: Informazioni su Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320465"
---
# <a name="about-media-foundation"></a>Informazioni su Media Foundation

Microsoft Media Foundation è la piattaforma multimediale di nuova generazione per Windows che consente a sviluppatori, consumer e provider di contenuti di adottare la nuova onda di contenuti Premium con affidabilità avanzata, qualità impareggiabile e interoperabilità senza problemi.

Media Foundation richiede Windows Vista o versione successiva. Usa il modello COM (Component Object Model) e richiede C/C++. Microsoft non fornisce un'API gestita per Media Foundation.

Le API Media Foundation fanno parte del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Per sviluppare un'applicazione Media Foundation, installare la versione più recente del Windows SDK.

## <a name="audio-and-video-quality"></a>Qualità audio e video

Media Foundation è stato progettato per soddisfare le sfide poste dal contenuto ad alta definizione. I miglioramenti apportati alla qualità audio e video in tutta la piattaforma consentono ora di offrire un'esperienza ottimale per il contenuto ad alta definizione di prossima generazione.

-   DirectX Video Acceleration (DXVA) 2,0 offre un'accelerazione video più efficiente, rispetto a DXVA 1,0, con la decodifica video più solida e semplificata e l'uso esteso dell'hardware nell'elaborazione video. Con DXVA 2,0, Windows è in grado di gestire alcuni dei più complessi contenuti ad alta definizione con elevata qualità e una resilienza migliorata.

-   Le informazioni sullo spazio dei colori vengono mantenute in tutta la pipeline video. Gli utenti possono usufruire di contenuti video con la massima fedeltà. Le informazioni sul colore e le immagini interlacciate vengono ora passate all'hardware per le composizioni a singolo passaggio. La conservazione delle informazioni sullo spazio dei colori riduce anche le conversioni dello spazio dei colori non necessarie, che consente di liberare più cicli per elaborare contenuti HD complessi.
-   Il renderer video avanzato (EVR) offre supporto temporizzato migliore, elaborazione video avanzata e resilienza migliorata. Il supporto per la riproduzione a schermo intero è stato migliorato e la rimozione dei video in modalità finestra è stata ridotta a icona.
-   Media Foundation usa il servizio Utilità di pianificazione classi multimediali (MMCSS), un nuovo servizio di sistema in Windows Vista. MMCSS consente alle applicazioni multimediali di garantire che l'elaborazione sensibile al tempo riceva l'accesso in ordine di priorità alle risorse della CPU.

## <a name="content-access"></a>Accesso al contenuto

Quando l'intrattenimento digitale passa all'era e il contenuto di definizione elevata diventa più portabile e onnipresente, la protezione del contenuto diventerà parte integrante dei prodotti multimediali digitali. L'estendibilità di Media Foundation garantisce che sia in grado di supportare tali tendenze.

Inoltre, Media Foundation estensibilità consente il funzionamento combinato di diversi sistemi di protezione del contenuto.

## <a name="about-media-foundation"></a>Informazioni su Media Foundation

Questa sezione contiene informazioni generali sulle API Media Foundation. Informazioni dettagliate sulla programmazione sono disponibili nella [Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md).



| Sezione                                                                              | Descrizione                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Novità di Media Foundation](whats-new-for-media-foundation.md)                | Vengono descritte le nuove funzionalità di Media Foundation.                               |
| [Intestazioni e librerie Media Foundation](media-foundation-headers-and-libraries.md) | Elenca i file di intestazione e di libreria che definiscono le API Media Foundation. |
| [Strumenti di Media Foundation](media-foundation-tools.md)                                 | Vengono descritti gli strumenti di sviluppo disponibili per Media Foundation.  |



 

Media Foundation non è incluso nelle edizioni N e KN di Windows 8. Per ulteriori informazioni, vedere [Microsoft Windows Media Feature Pack per le versioni N e KN di tutte le edizioni di Windows 8](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



