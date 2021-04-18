---
description: Segnala lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale ai componenti di integrazione di Hyper-V in esecuzione nella stessa macchina virtuale.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: Interfaccia IVmApplicationHealthMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309505"
---
# <a name="ivmapplicationhealthmonitor-interface"></a><span data-ttu-id="ee164-103">Interfaccia IVmApplicationHealthMonitor</span><span class="sxs-lookup"><span data-stu-id="ee164-103">IVmApplicationHealthMonitor interface</span></span>

<span data-ttu-id="ee164-104">Segnala lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale ai componenti di integrazione di Hyper-V in esecuzione nella stessa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ee164-104">Reports the health status of an application that is running in a virtual machine to the Hyper-V integration components running in the same virtual machine.</span></span> <span data-ttu-id="ee164-105">Lo stato delle applicazioni in esecuzione nella macchina virtuale si riflette nel  \[ \] valore della proprietà OperationalStatus 1 della classe [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="ee164-105">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span> <span data-ttu-id="ee164-106">Questa interfaccia fornisce anche un modo per reimpostare lo stato dell'applicazione accumulato in Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ee164-106">This interface also provides a way to reset all of the application state accumulated in Hyper-V.</span></span>

<span data-ttu-id="ee164-107">Questa interfaccia viene implementata dai componenti di integrazione di Hyper-V per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ee164-107">This interface is implemented by the Windows 8 Hyper-V integration components.</span></span> <span data-ttu-id="ee164-108">Un'istanza di questa interfaccia viene ottenuta creando un'istanza del CLSID **397a2e5f-348c-482d-b9a3-57d383b483cd** .</span><span class="sxs-lookup"><span data-stu-id="ee164-108">An instance of this interface is obtained by creating an instance of the **397a2e5f-348c-482d-b9a3-57d383b483cd** CLSID.</span></span>

## <a name="members"></a><span data-ttu-id="ee164-109">Membri</span><span class="sxs-lookup"><span data-stu-id="ee164-109">Members</span></span>

<span data-ttu-id="ee164-110">L'interfaccia **IVmApplicationHealthMonitor** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="ee164-110">The **IVmApplicationHealthMonitor** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ee164-111">**IVmApplicationHealthMonitor** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ee164-111">**IVmApplicationHealthMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="ee164-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="ee164-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ee164-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="ee164-113">Methods</span></span>

<span data-ttu-id="ee164-114">L'interfaccia **IVmApplicationHealthMonitor** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ee164-114">The **IVmApplicationHealthMonitor** interface has these methods.</span></span>



| <span data-ttu-id="ee164-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="ee164-115">Method</span></span>                                                                                   | <span data-ttu-id="ee164-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee164-116">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee164-117">**ResetAllApplicationState**</span><span class="sxs-lookup"><span data-stu-id="ee164-117">**ResetAllApplicationState**</span></span>](ivmapplicationhealthmonitor-resetallapplicationstate.md) | <span data-ttu-id="ee164-118">Reimposta lo stato di integrità di tutte le applicazioni in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ee164-118">Resets the health state for all applications in a virtual machine.</span></span><br/>            |
| [<span data-ttu-id="ee164-119">**SetApplicationState**</span><span class="sxs-lookup"><span data-stu-id="ee164-119">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)           | <span data-ttu-id="ee164-120">Imposta lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ee164-120">Sets the health state of an application that is running in a virtual machine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee164-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee164-121">Remarks</span></span>

<span data-ttu-id="ee164-122">Per utilizzare questo elemento di programmazione, è necessario installare i componenti di integrazione di Windows 8 nella macchina virtuale in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee164-122">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee164-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee164-123">Requirements</span></span>



| <span data-ttu-id="ee164-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee164-124">Requirement</span></span> | <span data-ttu-id="ee164-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ee164-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee164-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee164-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ee164-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ee164-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="ee164-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee164-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ee164-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ee164-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                           |
| <span data-ttu-id="ee164-130">Versione</span><span class="sxs-lookup"><span data-stu-id="ee164-130">Version</span></span><br/>                  | <span data-ttu-id="ee164-131">Componenti di integrazione per Windows 8</span><span class="sxs-lookup"><span data-stu-id="ee164-131">Integration components for Windows 8</span></span><br/>                                                                                                                                |
| <span data-ttu-id="ee164-132">IDL</span><span class="sxs-lookup"><span data-stu-id="ee164-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ee164-133"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee164-133"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ee164-134">IID</span><span class="sxs-lookup"><span data-stu-id="ee164-134">IID</span></span><br/>                      | <span data-ttu-id="ee164-135">IID \_ IVmApplicationHealthMonitor è definito come 267a0284-848f-447e-A096-5e10a1a76bca</span><span class="sxs-lookup"><span data-stu-id="ee164-135">IID\_IVmApplicationHealthMonitor is defined as 267a0284-848f-447e-a096-5e10a1a76bca</span></span><br/> <span data-ttu-id="ee164-136">Identificatore di oggetto definito come 397a2e5f-348c-482d-b9a3-57d383b483cd</span><span class="sxs-lookup"><span data-stu-id="ee164-136">Object Identifier is defined as 397a2e5f-348c-482d-b9a3-57d383b483cd</span></span><br/> |



 

