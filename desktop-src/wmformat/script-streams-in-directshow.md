---
title: Flussi di script in DirectShow
description: Flussi di script in DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, flussi di script
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Formati di sistema avanzati (ASF), flussi di script
- ASF (formato avanzato dei sistemi), flussi di script
- DirectShow, flussi di script
- flussi di script, DirectShow
- flussi, flussi di script in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332172"
---
# <a name="script-streams-in-directshow"></a>Flussi di script in DirectShow

Quando al filtro WM ASF Reader viene assegnato un file che include un flusso di tipo WMMEDIATYPE \_ script, viene creato un pin di output per esso che può essere connesso al filtro di rendering del comando script interno DirectShow. Quando si chiama **IGraphBuilder:: RenderFile**, il filtro viene aggiunto automaticamente al grafo e connesso. Quando il renderer interno del comando script riceve un esempio contenente un comando script, genera un **\_ \_ evento OLE EC** il cui **lParam** contiene lo script. L'applicazione è interamente responsabile della gestione di questo evento. Per ulteriori informazioni sull' **\_ \_ evento OLE EC**, vedere la documentazione di DirectShow SDK.

 

 




