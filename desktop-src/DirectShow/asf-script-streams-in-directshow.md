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
# <a name="asf-script-streams-in-directshow"></a><span data-ttu-id="58c29-103">Flussi di script ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="58c29-103">ASF Script Streams in DirectShow</span></span>

<span data-ttu-id="58c29-104">Quando al filtro [WM ASF Reader](wm-asf-reader-filter.md) viene assegnato un file che include un flusso di tipo WMMEDIATYPE \_ script, viene creato un pin di output che può essere connesso al filtro di [renderer del comando script interno](internal-script-command-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="58c29-104">When the [WM ASF Reader](wm-asf-reader-filter.md) filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="58c29-105">Quando si chiama [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), il filtro viene aggiunto automaticamente al grafo e connesso.</span><span class="sxs-lookup"><span data-stu-id="58c29-105">When you call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="58c29-106">Quando il renderer interno del comando script riceve un esempio contenente un comando script, genera un evento di [**\_ \_ evento OLE EC**](ec-ole-event.md) il cui *lParam* contiene lo script.</span><span class="sxs-lookup"><span data-stu-id="58c29-106">When the Internal Script Command Renderer receives a sample containing a script command, it fires an [**EC\_OLE\_EVENT**](ec-ole-event.md) event whose *lParam* contains the script.</span></span> <span data-ttu-id="58c29-107">L'applicazione è interamente responsabile della gestione di questo evento.</span><span class="sxs-lookup"><span data-stu-id="58c29-107">The application is entirely responsible for handling this event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58c29-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58c29-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58c29-109">Lettura di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="58c29-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



