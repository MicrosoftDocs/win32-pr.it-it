---
description: Definire il set di azioni per l' \_ archiviazione IOCTL \_ gestire il codice di controllo degli attributi del \_ set di dati \_ \_ .
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877749"
---
# <a name="device_data_management_set_action"></a><span data-ttu-id="7c83a-103">\_ \_ azione set di gestione dati \_ del \_ dispositivo</span><span class="sxs-lookup"><span data-stu-id="7c83a-103">DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION</span></span>

<span data-ttu-id="7c83a-104">I valori costanti seguenti sono il set di valori possibili per il tipo di **\_ \_ \_ \_ azione set di gestione dati del dispositivo** , definito come tipo **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="7c83a-104">The following constant values are the set of possible values for the **DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION** type, which is defined as type **DWORD**.</span></span>

<dl> <dt>

<span data-ttu-id="7c83a-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ None**</span><span class="sxs-lookup"><span data-stu-id="7c83a-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction\_None**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83a-106">0</span><span class="sxs-lookup"><span data-stu-id="7c83a-106">0</span></span>
</dt> <dt>



<span data-ttu-id="7c83a-107">Non viene eseguita alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="7c83a-107">No action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c83a-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction \_ Trim**</span><span class="sxs-lookup"><span data-stu-id="7c83a-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction\_Trim**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83a-109">1</span><span class="sxs-lookup"><span data-stu-id="7c83a-109">1</span></span>
</dt> <dt>



<span data-ttu-id="7c83a-110">Viene eseguita un'azione trim.</span><span class="sxs-lookup"><span data-stu-id="7c83a-110">A trim action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c83a-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**\_Notifica DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="7c83a-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**DeviceDsmAction\_Notification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83a-112">2 \| **DeviceDsmActionFlag non \_ distruttivo** (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="7c83a-112">2 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000002)</span></span>
</dt> <dt>



<span data-ttu-id="7c83a-113">Viene eseguita un'azione di notifica.</span><span class="sxs-lookup"><span data-stu-id="7c83a-113">A notification action is performed.</span></span> <span data-ttu-id="7c83a-114">I parametri si trovano in una struttura di [**\_ \_ \_ parametri di notifica DSM del dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) .</span><span class="sxs-lookup"><span data-stu-id="7c83a-114">The parameters are in a [**DEVICE\_DSM\_NOTIFICATION\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) structure.</span></span> <span data-ttu-id="7c83a-115">Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.</span><span class="sxs-lookup"><span data-stu-id="7c83a-115">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c83a-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**\_OffloadRead DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="7c83a-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction\_OffloadRead**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83a-117">3 \| **DeviceDsmActionFlag non \_ distruttivi** (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="7c83a-117">3 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000003)</span></span>
</dt> <dt>



<span data-ttu-id="7c83a-118">Viene eseguita un'azione di lettura offload.</span><span class="sxs-lookup"><span data-stu-id="7c83a-118">An offload read action is performed.</span></span> <span data-ttu-id="7c83a-119">I parametri si trovano in una struttura di [**\_ parametri di \_ \_ lettura \_ di OFFLOAD DSM del dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) .</span><span class="sxs-lookup"><span data-stu-id="7c83a-119">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_READ\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) structure.</span></span> <span data-ttu-id="7c83a-120">L'output si trova in una struttura di [**\_ \_ \_ output di lettura OFFLOAD archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) .</span><span class="sxs-lookup"><span data-stu-id="7c83a-120">The output is in a [**STORAGE\_OFFLOAD\_READ\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) structure.</span></span> <span data-ttu-id="7c83a-121">Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.</span><span class="sxs-lookup"><span data-stu-id="7c83a-121">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="7c83a-122">**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="7c83a-122">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c83a-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**\_OffloadWrite DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="7c83a-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction\_OffloadWrite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83a-124">4</span><span class="sxs-lookup"><span data-stu-id="7c83a-124">4</span></span>
</dt> <dt>



<span data-ttu-id="7c83a-125">Viene eseguita un'azione di scrittura di offload.</span><span class="sxs-lookup"><span data-stu-id="7c83a-125">An offload write action is performed.</span></span> <span data-ttu-id="7c83a-126">I parametri si trovano in una struttura di [**\_ parametri di \_ \_ scrittura \_ di OFFLOAD DSM del dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) .</span><span class="sxs-lookup"><span data-stu-id="7c83a-126">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_WRITE\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) structure.</span></span> <span data-ttu-id="7c83a-127">L'output si trova in una struttura di [**output di scrittura di OFFLOAD dell'archiviazione \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) .</span><span class="sxs-lookup"><span data-stu-id="7c83a-127">The output is in a [**STORAGE\_OFFLOAD\_WRITE\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) structure.</span></span>

<span data-ttu-id="7c83a-128">**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="7c83a-128">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c83a-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**Allocazione DeviceDsmAction \_**</span><span class="sxs-lookup"><span data-stu-id="7c83a-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**DeviceDsmAction\_Allocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83a-130">5 \| **DeviceDsmActionFlag non \_ distruttivi** (0x80000005)</span><span class="sxs-lookup"><span data-stu-id="7c83a-130">5 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000005)</span></span>
</dt> <dt>



<span data-ttu-id="7c83a-131">Viene restituita una bitmap di allocazione per il primo intervallo di set di dati passato.</span><span class="sxs-lookup"><span data-stu-id="7c83a-131">An allocation bitmap is returned for the first data set range passed in.</span></span> <span data-ttu-id="7c83a-132">L'output si trova in una struttura di [**\_ \_ \_ \_ \_ stato di provisioning LB del set di dati del dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) .</span><span class="sxs-lookup"><span data-stu-id="7c83a-132">The output is in a [**DEVICE\_DATA\_SET\_LB\_PROVISIONING\_STATE**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) structure.</span></span> <span data-ttu-id="7c83a-133">Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.</span><span class="sxs-lookup"><span data-stu-id="7c83a-133">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="7c83a-134">**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="7c83a-134">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c83a-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**\_Ripristino DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="7c83a-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**DeviceDsmAction\_Repair**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83a-136">6 \| **DeviceDsmActionFlag non \_ distruttivi** (0x80000006)</span><span class="sxs-lookup"><span data-stu-id="7c83a-136">6 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000006)</span></span>
</dt> <dt>



<span data-ttu-id="7c83a-137">Viene eseguita un'azione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7c83a-137">A repair action is performed.</span></span> <span data-ttu-id="7c83a-138">Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.</span><span class="sxs-lookup"><span data-stu-id="7c83a-138">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="7c83a-139">**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="7c83a-139">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c83a-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction \_ scrub**</span><span class="sxs-lookup"><span data-stu-id="7c83a-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction\_Scrub**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83a-141">7 \| **DeviceDsmActionFlag non \_ distruttivi** (0x80000007)</span><span class="sxs-lookup"><span data-stu-id="7c83a-141">7 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000007)</span></span>
</dt> <dt>



<span data-ttu-id="7c83a-142">Viene eseguita un'azione di scrub.</span><span class="sxs-lookup"><span data-stu-id="7c83a-142">A scrub action is performed.</span></span> <span data-ttu-id="7c83a-143">Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.</span><span class="sxs-lookup"><span data-stu-id="7c83a-143">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="7c83a-144">**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="7c83a-144">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7c83a-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**\_Resilienza DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="7c83a-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**DeviceDsmAction\_Resiliency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c83a-146">8 \| **DeviceDsmActionFlag non \_ distruttivi** (0x80000008)</span><span class="sxs-lookup"><span data-stu-id="7c83a-146">8 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000008)</span></span>
</dt> <dt>



<span data-ttu-id="7c83a-147">Viene eseguita un'azione di resilienza.</span><span class="sxs-lookup"><span data-stu-id="7c83a-147">A resiliency action is performed.</span></span> <span data-ttu-id="7c83a-148">Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.</span><span class="sxs-lookup"><span data-stu-id="7c83a-148">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="7c83a-149">**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="7c83a-149">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c83a-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c83a-150">Requirements</span></span>



| <span data-ttu-id="7c83a-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c83a-151">Requirement</span></span> | <span data-ttu-id="7c83a-152">Valore</span><span class="sxs-lookup"><span data-stu-id="7c83a-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c83a-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c83a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="7c83a-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c83a-154">Windows 7</span></span><br/>                                                                                      |
| <span data-ttu-id="7c83a-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c83a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="7c83a-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c83a-156">Windows Server 2008 R2</span></span><br/>                                                                         |
| <span data-ttu-id="7c83a-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c83a-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c83a-158"><dt>WinIoCtl. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c83a-158"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



 

 




