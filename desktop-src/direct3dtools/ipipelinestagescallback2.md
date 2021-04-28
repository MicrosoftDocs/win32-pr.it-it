---
description: '<span id="vspixengine.ipipelinestagescallback2"></span>Interfaccia IPipeLineStagesCallback2: non usata. In precedenza un callback per i dati delle fasi della pipeline.'
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
ms.openlocfilehash: 941a056a5c2af00cfa1bb53f038cbeb923a777bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097389"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span data-ttu-id="ee990-104"><span id="vspixengine.ipipelinestagescallback2"></span>Interfaccia IPipeLineStagesCallback2</span><span class="sxs-lookup"><span data-stu-id="ee990-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 interface</span></span>

<span data-ttu-id="ee990-105">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ee990-105">Not used.</span></span> <span data-ttu-id="ee990-106">In precedenza un callback per i dati delle fasi della pipeline.</span><span class="sxs-lookup"><span data-stu-id="ee990-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="ee990-107">Membri</span><span class="sxs-lookup"><span data-stu-id="ee990-107">Members</span></span>

<span data-ttu-id="ee990-108">**L'interfaccia IPipeLineStagesCallback2** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="ee990-108">The **IPipeLineStagesCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ee990-109">**IPipeLineStagesCallback2** include anche questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ee990-109">**IPipeLineStagesCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="ee990-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ee990-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ee990-111"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="ee990-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ee990-112">**L'interfaccia IPipeLineStagesCallback2** include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ee990-112">The **IPipeLineStagesCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ee990-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="ee990-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ee990-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee990-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ee990-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="ee990-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ee990-116">Callback che notifica all'host il numero di thread e gruppi dello shader di calcolo nella richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="ee990-116">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ee990-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="ee990-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ee990-118">Callback che notifica all'host che ThreadData non è disponibile per una fase e un evento della pipeline specifici.</span><span class="sxs-lookup"><span data-stu-id="ee990-118">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ee990-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee990-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ee990-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee990-120">Header</span></span></p></td><td><span data-ttu-id="ee990-121">Vspixengine.h</span><span class="sxs-lookup"><span data-stu-id="ee990-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
