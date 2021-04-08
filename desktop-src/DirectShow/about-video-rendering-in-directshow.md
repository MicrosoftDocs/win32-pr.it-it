---
description: Informazioni sul rendering video in DirectShow
ms.assetid: 3b064758-2ae5-4441-801c-5400e4ef3790
title: Informazioni sul rendering video in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699e8ecf133f362e699e6b9d650d11da5bf43347
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876974"
---
# <a name="about-video-rendering-in-directshow"></a>Informazioni sul rendering video in DirectShow

DirectShow fornisce diversi filtri che eseguono il rendering del video:

-   Filtro [renderer video](video-renderer-filter.md) . Questo filtro è disponibile per tutte le piattaforme che supportano DirectX e non prevede particolari requisiti di sistema. Il renderer video usa DirectDraw quando possibile per eseguire il rendering del video; in caso contrario, viene utilizzato GDI. Questo filtro è il renderer video predefinito sulle piattaforme precedenti a Windows XP.
-   [Filtro renderer video mixing 7](video-mixing-renderer-filter-7.md) (VMR-7). VMR-7 è disponibile in Windows XP, dove è il renderer video predefinito. VMR-7 usa sempre DirectDraw 7 per il rendering. Offre molte potenti funzionalità non disponibili nel filtro renderer video precedente, incluso un modello di plug-in in cui l'applicazione controlla le superfici DirectDraw usate per il rendering.
-   [Filtro renderer video mixing 9](video-mixing-renderer-filter-9.md) (VMR-9). VMR-9 è una versione più recente del renderer di mixaggio video che usa Direct3D 9 per il rendering. È disponibile per tutte le piattaforme che supportano DirectX. Tuttavia, non è il renderer predefinito, perché presenta requisiti di sistema più elevati rispetto al filtro renderer video.
-   Il filtro [Overlay Mixer](overlay-mixer-filter.md) è stato progettato specificamente per la riproduzione DVD e la trasmissione di video. Supporta anche VPEs (video Port Extensions), consentendo l'uso di decodificatori MPEG-2 hardware o sintonizzatori TV analoghi che inviano video direttamente alla scheda grafica.
-   Il filtro EVR ( [**Enhanced video renderer**](enhanced-video-renderer-filter.md) ) è disponibile a partire da Windows Vista. Offre prestazioni video migliorate rispetto ai renderer video precedenti, soprattutto quando è abilitata la composizione desktop di Windows Vista.

In genere, EVR è preferibile per le applicazioni destinate a Windows Vista o versioni successive e VMR-9 è preferibile per le applicazioni in esecuzione in versioni precedenti di Windows. Per ulteriori informazioni sull'utilizzo dei filtri VMR-7 e VMR-9, vedere [using the video Mixing Renderer](using-the-video-mixing-renderer.md).

Modalità finestra e modalità senza finestra

Un renderer video DirectShow può funzionare in modalità *finestra* o in modalità senza *finestra* .

-   In modalità finestra, il renderer crea la propria finestra per visualizzare il video. In genere si renderà questa finestra l'elemento figlio di una finestra dell'applicazione. Per altre informazioni, vedere [uso della modalità Window](using-windowed-mode.md).
-   In modalità senza finestra il renderer disegna il video direttamente su una finestra dell'applicazione. Non crea la propria finestra. Per altre informazioni su questa modalità, vedere [uso della modalità senza finestra](using-windowless-mode.md).

Il filtro renderer video supporta solo la modalità finestra. I filtri VMR-7 e VMR-9 supportano entrambe le modalità. Per la compatibilità con le versioni precedenti, per impostazione predefinita la modalità finestra è preferibile. EVR supporta solo la modalità senza finestra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering video](video-rendering.md)
</dt> </dl>

 

 



