---
title: Interfaccia IVMAccountant (VPCCOMInterfaces. h)
description: Consente di accedere alle informazioni relative all'accounting per una macchina virtuale.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- Interfaccia IVMAccountant Virtual PC
- Interfaccia IVMAccountant Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743474"
---
# <a name="ivmaccountant-interface"></a><span data-ttu-id="84be0-105">Interfaccia IVMAccountant</span><span class="sxs-lookup"><span data-stu-id="84be0-105">IVMAccountant interface</span></span>

<span data-ttu-id="84be0-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="84be0-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="84be0-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="84be0-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="84be0-108">Consente di accedere alle informazioni relative all'accounting per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84be0-108">Provides access to accounting-related information for a virtual machine.</span></span> <span data-ttu-id="84be0-109">Per recuperare **IVMAccountant** per una macchina virtuale, usare la proprietà [**IVMVirtualMachine:: Accountant**](ivmvirtualmachine-accountant.md) .</span><span class="sxs-lookup"><span data-stu-id="84be0-109">To retrieve the **IVMAccountant** for a virtual machine, use the [**IVMVirtualMachine::Accountant**](ivmvirtualmachine-accountant.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="84be0-110">Membri</span><span class="sxs-lookup"><span data-stu-id="84be0-110">Members</span></span>

<span data-ttu-id="84be0-111">L'interfaccia **IVMAccountant** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="84be0-111">The **IVMAccountant** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="84be0-112">**IVMAccountant** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="84be0-112">**IVMAccountant** also has these types of members:</span></span>

-   [<span data-ttu-id="84be0-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84be0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84be0-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84be0-114">Properties</span></span>

<span data-ttu-id="84be0-115">L'interfaccia **IVMAccountant** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="84be0-115">The **IVMAccountant** interface has these properties.</span></span>



| <span data-ttu-id="84be0-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84be0-116">Property</span></span>                                                                        | <span data-ttu-id="84be0-117">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="84be0-117">Access type</span></span>          | <span data-ttu-id="84be0-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84be0-118">Description</span></span>                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84be0-119">**CPUUtilization**</span><span class="sxs-lookup"><span data-stu-id="84be0-119">**CPUUtilization**</span></span>](ivmaccountant-cpuutilization.md)<br/>               | <span data-ttu-id="84be0-120">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="84be0-120">Read-only</span></span><br/> | <span data-ttu-id="84be0-121">Percentuale di utilizzo della CPU corrente per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84be0-121">The percentage of current CPU utilization for this virtual machine.</span></span><br/>                          |
| [<span data-ttu-id="84be0-122">**CPUUtilizationHistory**</span><span class="sxs-lookup"><span data-stu-id="84be0-122">**CPUUtilizationHistory**</span></span>](ivmaccountant-cpuutilizationhistory.md)<br/> | <span data-ttu-id="84be0-123">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="84be0-123">Read-only</span></span><br/> | <span data-ttu-id="84be0-124">L'utilizzo della CPU recente della macchina virtuale, come una matrice di valori percentuali.</span><span class="sxs-lookup"><span data-stu-id="84be0-124">The recent CPU utilization of this virtual machine (as an array of percentage values).</span></span><br/>       |
| [<span data-ttu-id="84be0-125">**DiskBytesRead**</span><span class="sxs-lookup"><span data-stu-id="84be0-125">**DiskBytesRead**</span></span>](ivmaccountant-diskbytesread.md)<br/>                 | <span data-ttu-id="84be0-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="84be0-126">Read-only</span></span><br/> | <span data-ttu-id="84be0-127">Il numero totale di byte letti da tutti i controller di archiviazione per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84be0-127">The total number of bytes read by all storage controllers for this virtual machine.</span></span><br/>          |
| [<span data-ttu-id="84be0-128">**DiskBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="84be0-128">**DiskBytesWritten**</span></span>](ivmaccountant-diskbyteswritten.md)<br/>           | <span data-ttu-id="84be0-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="84be0-129">Read-only</span></span><br/> | <span data-ttu-id="84be0-130">Il numero totale di byte scritti da tutti i controller di archiviazione per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84be0-130">The total number of bytes written by all storage controllers for this virtual machine.</span></span><br/>       |
| [<span data-ttu-id="84be0-131">**NetworkBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="84be0-131">**NetworkBytesReceived**</span></span>](ivmaccountant-networkbytesreceived.md)<br/>   | <span data-ttu-id="84be0-132">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="84be0-132">Read-only</span></span><br/> | <span data-ttu-id="84be0-133">Il numero totale di byte ricevuti da tutte le schede di rete virtuali per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84be0-133">The total number of bytes received by all virtual network adapters for this virtual machine.</span></span><br/> |
| [<span data-ttu-id="84be0-134">**NetworkBytesSent**</span><span class="sxs-lookup"><span data-stu-id="84be0-134">**NetworkBytesSent**</span></span>](ivmaccountant-networkbytessent.md)<br/>           | <span data-ttu-id="84be0-135">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="84be0-135">Read-only</span></span><br/> | <span data-ttu-id="84be0-136">Numero totale di byte inviati da tutte le schede di rete virtuali per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84be0-136">The total number of bytes sent by all virtual network adapters for this virtual machine.</span></span><br/>     |
| [<span data-ttu-id="84be0-137">**Tempo**</span><span class="sxs-lookup"><span data-stu-id="84be0-137">**UpTime**</span></span>](ivmaccountant-uptime.md)<br/>                               | <span data-ttu-id="84be0-138">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="84be0-138">Read-only</span></span><br/> | <span data-ttu-id="84be0-139">Numero di secondi di esecuzione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84be0-139">The number of seconds that the virtual machine has been running.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="84be0-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84be0-140">Requirements</span></span>



| <span data-ttu-id="84be0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="84be0-141">Requirement</span></span> | <span data-ttu-id="84be0-142">Valore</span><span class="sxs-lookup"><span data-stu-id="84be0-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="84be0-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84be0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="84be0-144">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="84be0-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84be0-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84be0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="84be0-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="84be0-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="84be0-147">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="84be0-147">End of client support</span></span><br/>    | <span data-ttu-id="84be0-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="84be0-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="84be0-149">Prodotto</span><span class="sxs-lookup"><span data-stu-id="84be0-149">Product</span></span><br/>                  | <span data-ttu-id="84be0-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="84be0-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="84be0-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84be0-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="84be0-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="84be0-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="84be0-153">IID</span><span class="sxs-lookup"><span data-stu-id="84be0-153">IID</span></span><br/>                      | <span data-ttu-id="84be0-154">IID \_ IVMAccountant è definito come 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="84be0-154">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



 

