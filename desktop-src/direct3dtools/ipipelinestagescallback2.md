---
description: Non usato. In precedenza un callback per i dati delle fasi della pipeline.
MS-HAID: vspixengine.IPipeLineStagesCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPipeLineStagesCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C27F94D2-D038-4D4E-9445-D0FF4C17F769
api_name:
- IPipeLineStagesCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d14e080d4381405f32c6def51d8c64d78aaa422
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965584"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span data-ttu-id="fbe87-104"><span id="vspixengine.ipipelinestagescallback2"></span>Interfaccia IPipeLineStagesCallback2</span><span class="sxs-lookup"><span data-stu-id="fbe87-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 interface</span></span>

<span data-ttu-id="fbe87-105">Non usato.</span><span class="sxs-lookup"><span data-stu-id="fbe87-105">Not used.</span></span> <span data-ttu-id="fbe87-106">In precedenza un callback per i dati delle fasi della pipeline.</span><span class="sxs-lookup"><span data-stu-id="fbe87-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="fbe87-107">Membri</span><span class="sxs-lookup"><span data-stu-id="fbe87-107">Members</span></span>

<span data-ttu-id="fbe87-108">L'interfaccia **IPipeLineStagesCallback2** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fbe87-108">The **IPipeLineStagesCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fbe87-109">**IPipeLineStagesCallback2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fbe87-109">**IPipeLineStagesCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="fbe87-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="fbe87-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="fbe87-111"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="fbe87-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="fbe87-112">L'interfaccia **IPipeLineStagesCallback2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="fbe87-112">The **IPipeLineStagesCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="fbe87-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="fbe87-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="fbe87-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbe87-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="fbe87-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbe87-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fbe87-116">Callback che notifica all'host il numero di thread e gruppi del compute shader nella richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="fbe87-116">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="fbe87-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbe87-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fbe87-118">Callback che notifica all'host che ThreadData non è disponibile per una particolare fase della pipeline ed evento.</span><span class="sxs-lookup"><span data-stu-id="fbe87-118">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="fbe87-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbe87-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fbe87-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fbe87-120">Header</span></span></p></td><td><span data-ttu-id="fbe87-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fbe87-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
