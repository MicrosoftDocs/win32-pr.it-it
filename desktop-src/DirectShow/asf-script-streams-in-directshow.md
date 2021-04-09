---
description: Flussi di script ASF in DirectShow
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: Flussi di script ASF in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965769"
---
# <a name="asf-script-streams-in-directshow"></a>Flussi di script ASF in DirectShow

Quando al filtro [WM ASF Reader](wm-asf-reader-filter.md) viene assegnato un file che include un flusso di tipo WMMEDIATYPE \_ script, viene creato un pin di output che può essere connesso al filtro di [renderer del comando script interno](internal-script-command-renderer-filter.md) . Quando si chiama [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), il filtro viene aggiunto automaticamente al grafo e connesso. Quando il renderer interno del comando script riceve un esempio contenente un comando script, genera un evento di [**\_ \_ evento OLE EC**](ec-ole-event.md) il cui *lParam* contiene lo script. L'applicazione è interamente responsabile della gestione di questo evento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



