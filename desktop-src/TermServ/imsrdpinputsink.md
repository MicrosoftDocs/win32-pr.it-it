---
title: Interfaccia IMsRdpInputSink
description: Sink di input desktop remoto.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpInputSink Servizi Desktop remoto
- Interfaccia IMsRdpInputSink Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3112b3bb6df92bfb7e403e779773a2203f2cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963968"
---
# <a name="imsrdpinputsink-interface"></a><span data-ttu-id="3b40b-105">Interfaccia IMsRdpInputSink</span><span class="sxs-lookup"><span data-stu-id="3b40b-105">IMsRdpInputSink interface</span></span>

<span data-ttu-id="3b40b-106">Sink di input desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="3b40b-106">Remote desktop input sink.</span></span>

## <a name="members"></a><span data-ttu-id="3b40b-107">Membri</span><span class="sxs-lookup"><span data-stu-id="3b40b-107">Members</span></span>

<span data-ttu-id="3b40b-108">L'interfaccia **IMsRdpInputSink** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3b40b-108">The **IMsRdpInputSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3b40b-109">**IMsRdpInputSink** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3b40b-109">**IMsRdpInputSink** also has these types of members:</span></span>

-   [<span data-ttu-id="3b40b-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="3b40b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3b40b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="3b40b-111">Methods</span></span>

<span data-ttu-id="3b40b-112">L'interfaccia **IMsRdpInputSink** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3b40b-112">The **IMsRdpInputSink** interface has these methods.</span></span>



| <span data-ttu-id="3b40b-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="3b40b-113">Method</span></span>                                                               | <span data-ttu-id="3b40b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b40b-114">Description</span></span>                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| <span data-ttu-id="3b40b-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b40b-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span></span>               | <span data-ttu-id="3b40b-116">Aggiunge l'input tocco.</span><span class="sxs-lookup"><span data-stu-id="3b40b-116">Adds touch input.</span></span><br/>         |
| <span data-ttu-id="3b40b-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b40b-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span></span>           | <span data-ttu-id="3b40b-118">Inizio tocco frame.</span><span class="sxs-lookup"><span data-stu-id="3b40b-118">Begin touch frame.</span></span><br/>        |
| <span data-ttu-id="3b40b-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b40b-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span></span>               | <span data-ttu-id="3b40b-120">Termina il frame touch.</span><span class="sxs-lookup"><span data-stu-id="3b40b-120">End touch frame.</span></span><br/>          |
| <span data-ttu-id="3b40b-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b40b-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span></span>       | <span data-ttu-id="3b40b-122">Invia l'evento della tastiera.</span><span class="sxs-lookup"><span data-stu-id="3b40b-122">Sends keyboard event.</span></span><br/>     |
| <span data-ttu-id="3b40b-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b40b-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span></span> | <span data-ttu-id="3b40b-124">Invia l'evento del pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="3b40b-124">Sends mouse button event.</span></span><br/> |
| <span data-ttu-id="3b40b-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b40b-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span></span>     | <span data-ttu-id="3b40b-126">Invia l'evento di spostamento del mouse.</span><span class="sxs-lookup"><span data-stu-id="3b40b-126">Sends mouse move event.</span></span><br/>   |
| <span data-ttu-id="3b40b-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b40b-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span></span>   | <span data-ttu-id="3b40b-128">Invia l'evento della rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="3b40b-128">Sends mouse wheel event.</span></span><br/>  |
| <span data-ttu-id="3b40b-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b40b-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span></span>               | <span data-ttu-id="3b40b-130">Invia l'evento di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3b40b-130">Sends sync event.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="3b40b-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b40b-131">Requirements</span></span>



| <span data-ttu-id="3b40b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b40b-132">Requirement</span></span> | <span data-ttu-id="3b40b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="3b40b-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b40b-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b40b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3b40b-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3b40b-135">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="3b40b-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b40b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3b40b-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3b40b-137">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="3b40b-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3b40b-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b40b-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b40b-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b40b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3b40b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b40b-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b40b-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b40b-142">IID</span><span class="sxs-lookup"><span data-stu-id="3b40b-142">IID</span></span><br/>                      | <span data-ttu-id="3b40b-143">IID \_ IMsRdpInputSink è definito come 4606850E-76A7-4E28-A47E-C7174F619351</span><span class="sxs-lookup"><span data-stu-id="3b40b-143">IID\_IMsRdpInputSink is defined as 4606850E-76A7-4E28-A47E-C7174F619351</span></span><br/>     |



 

