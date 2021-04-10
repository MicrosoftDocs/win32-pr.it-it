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
# <a name="script-streams-in-directshow"></a><span data-ttu-id="439f0-112">Flussi di script in DirectShow</span><span class="sxs-lookup"><span data-stu-id="439f0-112">Script Streams in DirectShow</span></span>

<span data-ttu-id="439f0-113">Quando al filtro WM ASF Reader viene assegnato un file che include un flusso di tipo WMMEDIATYPE \_ script, viene creato un pin di output per esso che può essere connesso al filtro di rendering del comando script interno DirectShow.</span><span class="sxs-lookup"><span data-stu-id="439f0-113">When the WM ASF Reader filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the DirectShow Internal Script Command Renderer filter.</span></span> <span data-ttu-id="439f0-114">Quando si chiama **IGraphBuilder:: RenderFile**, il filtro viene aggiunto automaticamente al grafo e connesso.</span><span class="sxs-lookup"><span data-stu-id="439f0-114">When you call **IGraphBuilder::RenderFile**, that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="439f0-115">Quando il renderer interno del comando script riceve un esempio contenente un comando script, genera un **\_ \_ evento OLE EC** il cui **lParam** contiene lo script.</span><span class="sxs-lookup"><span data-stu-id="439f0-115">When the Internal Script Command Renderer receives a sample containing a script command, it fires an **EC\_OLE\_EVENT** whose **lParam** contains the script.</span></span> <span data-ttu-id="439f0-116">L'applicazione è interamente responsabile della gestione di questo evento.</span><span class="sxs-lookup"><span data-stu-id="439f0-116">The application is entirely responsible for handling this event.</span></span> <span data-ttu-id="439f0-117">Per ulteriori informazioni sull' **\_ \_ evento OLE EC**, vedere la documentazione di DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="439f0-117">For more information on **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

 

 




