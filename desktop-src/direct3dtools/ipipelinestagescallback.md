---
description: Non usato. In precedenza un callback per i dati delle fasi della pipeline.
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPipeLineStagesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a00815fc42f4ac7b56e310fafedc0561f40233
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876993"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span data-ttu-id="8f683-104"><span id="vspixengine.ipipelinestagescallback"></span>Interfaccia IPipeLineStagesCallback</span><span class="sxs-lookup"><span data-stu-id="8f683-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback interface</span></span>

<span data-ttu-id="8f683-105">Non usato.</span><span class="sxs-lookup"><span data-stu-id="8f683-105">Not used.</span></span> <span data-ttu-id="8f683-106">In precedenza un callback per i dati delle fasi della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f683-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="8f683-107">Membri</span><span class="sxs-lookup"><span data-stu-id="8f683-107">Members</span></span>

<span data-ttu-id="8f683-108">L'interfaccia **IPipeLineStagesCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8f683-108">The **IPipeLineStagesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8f683-109">**IPipeLineStagesCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8f683-109">**IPipeLineStagesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="8f683-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="8f683-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="8f683-111"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="8f683-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="8f683-112">L'interfaccia **IPipeLineStagesCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8f683-112">The **IPipeLineStagesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="8f683-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="8f683-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="8f683-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f683-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="8f683-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f683-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="8f683-116">Callback che notifica all'host le fasi della pipeline utilizzate dalla chiamata di richiamo della richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="8f683-116">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="8f683-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f683-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="8f683-118">Callback che notifica all'host che le fasi della pipeline non sono in grado di restituire i dati mesh per l'evento specificato nella richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="8f683-118">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="8f683-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f683-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="8f683-120">Callback che notifica all'host delle fasi della pipeline le informazioni mesh restituite dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="8f683-120">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="8f683-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f683-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="8f683-122">Callback che notifica all'host le informazioni sull'immagine delle fasi della pipeline restituite dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="8f683-122">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="8f683-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f683-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8f683-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f683-124">Header</span></span></p></td><td><span data-ttu-id="8f683-125">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8f683-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
