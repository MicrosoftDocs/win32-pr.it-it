---
description: Interfaccia originale per la comunicazione di dati relativi a un vsglog.
MS-HAID: vspixengine.IPixEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPixEngine
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87AB1D07-8E90-49F0-B44D-F6185923B8D4
api_name:
- IPixEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2f02538f7acbd88daf166af657382e507a4e5661
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482644"
---
# <a name="span-idvspixengineipixenginespanipixengine-interface"></a><span data-ttu-id="01234-103"><span id="vspixengine.ipixengine"></span>Interfaccia IPixEngine</span><span class="sxs-lookup"><span data-stu-id="01234-103"><span id="vspixengine.ipixengine"></span>IPixEngine interface</span></span>

<span data-ttu-id="01234-104">Interfaccia originale per la comunicazione di dati relativi a un vsglog.</span><span class="sxs-lookup"><span data-stu-id="01234-104">Original interface for communicating data about a vsglog .</span></span>

## <a name="members"></a><span data-ttu-id="01234-105">Membri</span><span class="sxs-lookup"><span data-stu-id="01234-105">Members</span></span>

<span data-ttu-id="01234-106">L'interfaccia **IPixEngine** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="01234-106">The **IPixEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="01234-107">**IPixEngine** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="01234-107">**IPixEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="01234-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="01234-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="01234-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="01234-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="01234-110">L'interfaccia **IPixEngine** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="01234-110">The **IPixEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="01234-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="01234-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="01234-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01234-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="01234-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="01234-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="01234-114">Apre un log di grafica.</span><span class="sxs-lookup"><span data-stu-id="01234-114">Opens a graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="01234-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></span><span class="sxs-lookup"><span data-stu-id="01234-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="01234-116">Esegue un esperimento.</span><span class="sxs-lookup"><span data-stu-id="01234-116">Runs an experiment.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="01234-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="01234-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="01234-118">Salva il log di grafica nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="01234-118">Saves the graphics log to the specified location.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="01234-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></span><span class="sxs-lookup"><span data-stu-id="01234-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="01234-120">Non usato.</span><span class="sxs-lookup"><span data-stu-id="01234-120">Not used.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="01234-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>Arresto</strong></a></span><span class="sxs-lookup"><span data-stu-id="01234-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>ShutDown</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="01234-122">Arresta il motore.</span><span class="sxs-lookup"><span data-stu-id="01234-122">Shuts down the engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="01234-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01234-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="01234-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01234-124">Header</span></span></p></td><td><span data-ttu-id="01234-125">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="01234-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
