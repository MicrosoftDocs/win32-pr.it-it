---
description: Informazioni sul rendering video in DirectShow
ms.assetid: 3b064758-2ae5-4441-801c-5400e4ef3790
title: Informazioni sul rendering video in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d2d39cab75f2943a052b157296673f504a1220c17369d5a1639215f074a359
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873671"
---
# <a name="about-video-rendering-in-directshow"></a>Informazioni sul rendering video in DirectShow

DirectShow fornisce diversi filtri che eseguono il rendering del video:

-   [Filtro renderer](video-renderer-filter.md) video. Questo filtro è disponibile per tutte le piattaforme che supportano DirectX e non presenta particolari requisiti di sistema. Il renderer video usa DirectDraw quando possibile per eseguire il rendering del video. In caso contrario, usa GDI. Questo filtro è il renderer video predefinito nelle piattaforme precedenti a Windows XP.
-   [Filtro del renderer di combinazione video 7](video-mixing-renderer-filter-7.md) (VMR-7). VMR-7 è disponibile in Windows XP, dove è il renderer video predefinito. VMR-7 usa sempre DirectDraw 7 per il rendering. Offre molte potenti funzionalità non disponibili nel filtro del renderer video precedente, incluso un modello di plug-in in cui l'applicazione controlla le superfici DirectDraw usate per il rendering.
-   [Filtro del renderer di combinazione video 9](video-mixing-renderer-filter-9.md) (VMR-9). VMR-9 è una versione più recente del renderer di combinazione video che usa Direct3D 9 per il rendering. È disponibile per tutte le piattaforme che supportano DirectX. Non è tuttavia il renderer predefinito, perché presenta requisiti di sistema più elevati rispetto al filtro del renderer video.
-   Il [filtro di Mixer](overlay-mixer-filter.md) sovrimpressione è progettato in modo specifico per la riproduzione di DVD e la trasmissione di video. Supporta anche le estensioni della porta video (VPE), consentendone l'uso con decodificatori MPEG-2 hardware o ottimizzatori TV analogici che inviano video direttamente alla scheda grafica.
-   Il [**filtro Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) è disponibile a partire da Windows Vista. Offre prestazioni video migliorate rispetto ai renderer video precedenti, soprattutto quando Windows la composizione desktop di Vista è abilitata.

In genere, EVR è preferibile per le applicazioni che hanno come destinazione Windows Vista o versioni successive e VMR-9 è preferibile per le applicazioni in esecuzione in versioni precedenti di Windows. Per altre informazioni sull'uso dei filtri VMR-7 e VMR-9, vedere Uso del [renderer di](using-the-video-mixing-renderer.md)combinazione video.

Modalità finestra e modalità senza finestra

Un DirectShow renderer video può funzionare in *modalità finestra* o *senza* finestra.

-   In modalità finestra il renderer crea la propria finestra per visualizzare il video. In genere si rende questa finestra l'elemento figlio di una finestra dell'applicazione. Per altre informazioni, vedere [Uso della modalità finestra.](using-windowed-mode.md)
-   In modalità senza finestra, il renderer disegna il video direttamente in una finestra dell'applicazione. Non crea una finestra propria. Per altre informazioni su questa modalità, vedere [Uso della modalità senza finestra.](using-windowless-mode.md)

Il filtro Renderer video supporta solo la modalità finestra. I filtri VMR-7 e VMR-9 supportano entrambe le modalità. Per impostazione predefinita, viene impostata la modalità finestra per compatibilità con le versioni precedenti, ma è preferibile la modalità senza finestra. EVR supporta solo la modalità senza finestra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video Rendering](video-rendering.md)
</dt> </dl>

 

 



