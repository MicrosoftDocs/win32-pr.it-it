---
description: Implementato dal browser. Espone metodi che gestiscono il monitoraggio che contiene la barra delle applicazioni di Windows in un sistema a più monitor.
title: Interfaccia IMultiMonitorDockingSite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995197"
---
# <a name="imultimonitordockingsite-interface"></a><span data-ttu-id="805f5-104">Interfaccia IMultiMonitorDockingSite</span><span class="sxs-lookup"><span data-stu-id="805f5-104">IMultiMonitorDockingSite interface</span></span>

<span data-ttu-id="805f5-105">Implementato dal browser.</span><span class="sxs-lookup"><span data-stu-id="805f5-105">Implemented by the browser.</span></span> <span data-ttu-id="805f5-106">Espone metodi che gestiscono il monitoraggio che contiene la barra delle applicazioni di Windows in un sistema a più monitor.</span><span class="sxs-lookup"><span data-stu-id="805f5-106">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span>

## <a name="members"></a><span data-ttu-id="805f5-107">Membri</span><span class="sxs-lookup"><span data-stu-id="805f5-107">Members</span></span>

<span data-ttu-id="805f5-108">L'interfaccia **IMultiMonitorDockingSite** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="805f5-108">The **IMultiMonitorDockingSite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="805f5-109">**IMultiMonitorDockingSite** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="805f5-109">**IMultiMonitorDockingSite** also has these types of members:</span></span>

-   [<span data-ttu-id="805f5-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="805f5-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="805f5-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="805f5-111">Methods</span></span>

<span data-ttu-id="805f5-112">L'interfaccia **IMultiMonitorDockingSite** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="805f5-112">The **IMultiMonitorDockingSite** interface has these methods.</span></span>



| <span data-ttu-id="805f5-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="805f5-113">Method</span></span>                                                            | <span data-ttu-id="805f5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="805f5-114">Description</span></span>                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="805f5-115">**Getmonitor**</span><span class="sxs-lookup"><span data-stu-id="805f5-115">**GetMonitor**</span></span>](imultimonitordockingsite-getmonitor.md)         | <span data-ttu-id="805f5-116">Ottiene il monitoraggio predefinito corrente.</span><span class="sxs-lookup"><span data-stu-id="805f5-116">Gets the current default monitor.</span></span><br/>                                               |
| [<span data-ttu-id="805f5-117">**RequestMonitor**</span><span class="sxs-lookup"><span data-stu-id="805f5-117">**RequestMonitor**</span></span>](imultimonitordockingsite-requestmonitor.md) | <span data-ttu-id="805f5-118">Verifica che il monitoraggio sia attivo e disponibile.</span><span class="sxs-lookup"><span data-stu-id="805f5-118">Verifies that the monitor is active and available.</span></span><br/>                              |
| [<span data-ttu-id="805f5-119">**Monitoraggio di**</span><span class="sxs-lookup"><span data-stu-id="805f5-119">**SetMonitor**</span></span>](imultimonitordockingsite-setmonitor.md)         | <span data-ttu-id="805f5-120">Modifica il monitoraggio usato per le barre degli strumenti ancorate in un sistema a più monitor.</span><span class="sxs-lookup"><span data-stu-id="805f5-120">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="805f5-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="805f5-121">Remarks</span></span>

<span data-ttu-id="805f5-122">In genere l'interfaccia **IMultiMonitorDockingSite** non viene implementata.</span><span class="sxs-lookup"><span data-stu-id="805f5-122">You do not typically implement the **IMultiMonitorDockingSite** interface.</span></span> <span data-ttu-id="805f5-123">Il browser della shell implementa questa interfaccia per supportare più monitor.</span><span class="sxs-lookup"><span data-stu-id="805f5-123">The Shell browser implements this interface to support multiple monitors.</span></span>

## <a name="requirements"></a><span data-ttu-id="805f5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="805f5-124">Requirements</span></span>



| <span data-ttu-id="805f5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="805f5-125">Requirement</span></span> | <span data-ttu-id="805f5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="805f5-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="805f5-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="805f5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="805f5-128">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="805f5-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="805f5-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="805f5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="805f5-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="805f5-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
