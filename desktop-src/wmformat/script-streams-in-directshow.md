---
title: Script Flussi in DirectShow
description: Script Flussi in DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows Media Format SDK,DirectShow
- Windows MEDIA Format SDK, flussi di script
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), flussi di script
- ASF (Advanced Systems Format), flussi di script
- DirectShow, flussi di script
- flussi di script, DirectShow
- flussi, flussi di script in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30e832928b84ab0e1e755dcfdb8c79893c5d942e15e4beb9925f852251614bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929620"
---
# <a name="script-streams-in-directshow"></a>Script Flussi in DirectShow

Quando al filtro lettore ASF WM viene assegnato un file che include un flusso di tipo Script WMMEDIATYPE, viene creato un pin di output per il filtro che può essere connesso al filtro del renderer del comando script interno di \_ DirectShow. Quando si chiama **IGraphBuilder::RenderFile,** il filtro viene aggiunto automaticamente al grafo e connesso. Quando il renderer del comando script interno riceve un esempio contenente un comando script, genera un EVENTO **\_ OLE \_ EC** il cui **lParam** contiene lo script. L'applicazione è interamente responsabile della gestione di questo evento. Per altre informazioni su **EC \_ OLE \_ EVENT,** vedere la documentazione DirectShow SDK.

 

 




