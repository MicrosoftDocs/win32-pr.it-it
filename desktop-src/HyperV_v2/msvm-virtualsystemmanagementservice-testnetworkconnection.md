---
description: Verifica la connettività di rete di una macchina virtuale in un ambiente di virtualizzazione rete Windows.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Metodo TestNetworkConnection della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e8f15faacb1b8ad683b1ea9abfa9b91f5c376dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128399"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="3d85b-103">Metodo TestNetworkConnection della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="3d85b-103">TestNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="3d85b-104">Verifica la connettività di rete di una macchina virtuale in un ambiente di virtualizzazione rete Windows.</span><span class="sxs-lookup"><span data-stu-id="3d85b-104">Tests the network connectivity of a VM in a Windows network virtualization environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d85b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d85b-105">Syntax</span></span>


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3d85b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d85b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d85b-107">*TargetNetworkAdapter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d85b-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d85b-108">Riferimento a un [**\_ EthernetPortAllocationSettingData MSVM**](msvm-ethernetportallocationsettingdata.md) che descrive la scheda di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3d85b-108">Reference to a [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) describing the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3d85b-109">Il *mittenti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d85b-109">*IsSender* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d85b-110">Indica se questo metodo viene richiamato al mittente o al ricevitore.</span><span class="sxs-lookup"><span data-stu-id="3d85b-110">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="3d85b-111">*SenderIP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d85b-111">*SenderIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d85b-112">Indirizzo IP del mittente.</span><span class="sxs-lookup"><span data-stu-id="3d85b-112">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3d85b-113">*ReceiverIP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d85b-113">*ReceiverIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d85b-114">Indirizzo MAC del mittente.</span><span class="sxs-lookup"><span data-stu-id="3d85b-114">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="3d85b-115">*ReceiverMac* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d85b-115">*ReceiverMac* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d85b-116">Indirizzo MAC del mittente.</span><span class="sxs-lookup"><span data-stu-id="3d85b-116">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="3d85b-117">*IsolationId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d85b-117">*IsolationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d85b-118">ID isolamento.</span><span class="sxs-lookup"><span data-stu-id="3d85b-118">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="3d85b-119">*SequenceNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d85b-119">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d85b-120">ID isolamento.</span><span class="sxs-lookup"><span data-stu-id="3d85b-120">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="3d85b-121">*RoundtripTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d85b-121">*RoundTripTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d85b-122">Round trip tempo.</span><span class="sxs-lookup"><span data-stu-id="3d85b-122">The round trip time.</span></span>

</dd> <dt>

<span data-ttu-id="3d85b-123">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3d85b-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d85b-124">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3d85b-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d85b-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d85b-125">Return value</span></span>

<span data-ttu-id="3d85b-126">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d85b-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3d85b-127">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="3d85b-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3d85b-128">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="3d85b-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3d85b-129">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="3d85b-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3d85b-130">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="3d85b-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3d85b-131">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="3d85b-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3d85b-132">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="3d85b-132">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3d85b-133">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="3d85b-133">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3d85b-134">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3d85b-134">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3d85b-135">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3d85b-135">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3d85b-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d85b-136">Requirements</span></span>



| <span data-ttu-id="3d85b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d85b-137">Requirement</span></span> | <span data-ttu-id="3d85b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="3d85b-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d85b-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d85b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3d85b-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3d85b-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3d85b-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d85b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3d85b-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3d85b-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3d85b-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3d85b-143">Namespace</span></span><br/>                | <span data-ttu-id="3d85b-144">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3d85b-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3d85b-145">MOF</span><span class="sxs-lookup"><span data-stu-id="3d85b-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d85b-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d85b-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d85b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3d85b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d85b-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3d85b-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3d85b-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d85b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d85b-150">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="3d85b-150">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

