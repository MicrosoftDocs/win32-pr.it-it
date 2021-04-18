---
description: Scelta del renderer video corretto
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Scelta del renderer video corretto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304330"
---
# <a name="choosing-the-right-video-renderer"></a>Scelta del renderer video corretto

DirectShow fornisce diversi filtri per renderer video, riepilogati nella tabella seguente.



| Filtra                                                                  | Commenti                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| [**Renderer video migliorato**](enhanced-video-renderer-filter.md) (EVR) | USA Direct3D 9. Richiede Windows Vista o versione successiva. |
| [Renderer di mixaggio video 9](video-mixing-renderer-filter-9.md) (VMR-9)   | USA Direct3D 9. Richiede Windows XP o versione successiva.    |
| [Filtro di mixaggio video 7](video-mixing-renderer-filter-7.md) (VMR-7)     | Usa DirectDraw. Richiede Windows XP o versione successiva.    |
| [Mixer overlay](using-the-overlay-mixer-in-video-capture.md)           | Supporta le sovrapposizioni hardware tramite DirectDraw.    |
| Filtro [renderer video](video-renderer-filter.md) legacy.              | Usa DirectDraw o (raramente) GDI                   |



 

Il renderer da usare dipende in gran parte dalle versioni di Windows che è necessario supportare.

-   In Windows Vista e versioni successive, le applicazioni devono utilizzare EVR se l'hardware lo supporta. In caso contrario, eseguire il fallback a VMR-9 o VMR-7. Il EVR offre prestazioni migliori e una migliore qualità dei video rispetto ai renderer precedenti. Inoltre, è progettato per funzionare con la Gestione finestre desktop (DWM).
-   Prima di Windows Vista, utilizzare VMR-9 se l'hardware lo supporta e la funzionalità della porta video non è necessaria. In caso contrario, usare VMR-7.
-   Nei sistemi meno recenti potrebbe essere necessario usare il mixer overlay (per la porta video o il supporto della sovrimpressione hardware) o il filtro renderer video legacy.

Per impostazione predefinita, i metodi [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) e [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) usano VMR-7. Se l'hardware non supporta VMR-7, questi metodi eseguono il fallback al filtro renderer video legacy. EVR e VMR-9 non sono mai i renderer predefiniti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering video](video-rendering.md)
</dt> </dl>

 

 



