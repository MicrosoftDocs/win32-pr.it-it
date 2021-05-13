---
description: Implementato dal browser. Espone metodi che gestiscono quale monitoraggio contiene la barra delle applicazioni di Windows in un sistema a più monitor.
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
ms.openlocfilehash: 5ea3461d00c16f7384d7396e2f03946d517c460f
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841892"
---
# <a name="imultimonitordockingsite-interface"></a><span data-ttu-id="9612e-104">Interfaccia IMultiMonitorDockingSite</span><span class="sxs-lookup"><span data-stu-id="9612e-104">IMultiMonitorDockingSite interface</span></span>

<span data-ttu-id="9612e-105">Implementato dal browser.</span><span class="sxs-lookup"><span data-stu-id="9612e-105">Implemented by the browser.</span></span> <span data-ttu-id="9612e-106">Espone metodi che gestiscono quale monitoraggio contiene la barra delle applicazioni di Windows in un sistema a più monitor.</span><span class="sxs-lookup"><span data-stu-id="9612e-106">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span>

## <a name="members"></a><span data-ttu-id="9612e-107">Membri</span><span class="sxs-lookup"><span data-stu-id="9612e-107">Members</span></span>

<span data-ttu-id="9612e-108">**L'interfaccia IMultiMonitorDockingSite** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="9612e-108">The **IMultiMonitorDockingSite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9612e-109">**IMultiMonitorDockingSite** include anche questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9612e-109">**IMultiMonitorDockingSite** also has these types of members:</span></span>

-   [<span data-ttu-id="9612e-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="9612e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9612e-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="9612e-111">Methods</span></span>

<span data-ttu-id="9612e-112">**L'interfaccia IMultiMonitorDockingSite** include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9612e-112">The **IMultiMonitorDockingSite** interface has these methods.</span></span>



| <span data-ttu-id="9612e-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="9612e-113">Method</span></span>                                                            | <span data-ttu-id="9612e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9612e-114">Description</span></span>                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9612e-115">**GetMonitor**</span><span class="sxs-lookup"><span data-stu-id="9612e-115">**GetMonitor**</span></span>](imultimonitordockingsite-getmonitor.md)         | <span data-ttu-id="9612e-116">Ottiene il monitoraggio predefinito corrente.</span><span class="sxs-lookup"><span data-stu-id="9612e-116">Gets the current default monitor.</span></span><br/>                                               |
| [<span data-ttu-id="9612e-117">**RequestMonitor**</span><span class="sxs-lookup"><span data-stu-id="9612e-117">**RequestMonitor**</span></span>](imultimonitordockingsite-requestmonitor.md) | <span data-ttu-id="9612e-118">Verifica che il monitoraggio sia attivo e disponibile.</span><span class="sxs-lookup"><span data-stu-id="9612e-118">Verifies that the monitor is active and available.</span></span><br/>                              |
| [<span data-ttu-id="9612e-119">**SetMonitor**</span><span class="sxs-lookup"><span data-stu-id="9612e-119">**SetMonitor**</span></span>](imultimonitordockingsite-setmonitor.md)         | <span data-ttu-id="9612e-120">Modifica il monitor usato per le barre degli strumenti ancorate in un sistema a più monitor.</span><span class="sxs-lookup"><span data-stu-id="9612e-120">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9612e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="9612e-121">Remarks</span></span>

<span data-ttu-id="9612e-122">In genere non si implementa **l'interfaccia IMultiMonitorDockingSite.**</span><span class="sxs-lookup"><span data-stu-id="9612e-122">You do not typically implement the **IMultiMonitorDockingSite** interface.</span></span> <span data-ttu-id="9612e-123">Il browser shell implementa questa interfaccia per supportare più monitor.</span><span class="sxs-lookup"><span data-stu-id="9612e-123">The Shell browser implements this interface to support multiple monitors.</span></span>

## <a name="requirements"></a><span data-ttu-id="9612e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9612e-124">Requirements</span></span>



| <span data-ttu-id="9612e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9612e-125">Requirement</span></span> | <span data-ttu-id="9612e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9612e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="9612e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9612e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9612e-128">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9612e-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9612e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9612e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9612e-130">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9612e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
