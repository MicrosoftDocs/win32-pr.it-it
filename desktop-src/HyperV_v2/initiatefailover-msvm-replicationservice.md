---
description: Avvia un failover per una macchina virtuale in un'immagine dell'applicazione o del punto di replica standard.
ms.assetid: cd7e9398-c234-4637-906d-69b46ebf3f51
title: Metodo InitiateFailover della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f05a9b126028b741782d253ac12b79f9f88e1e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344541"
---
# <a name="initiatefailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="6c976-103">Metodo InitiateFailover della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="6c976-103">InitiateFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="6c976-104">Avvia un failover per una macchina virtuale in un'immagine dell'applicazione o del punto di replica standard.</span><span class="sxs-lookup"><span data-stu-id="6c976-104">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c976-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c976-105">Syntax</span></span>


```mof
uint32 InitiateFailover(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6c976-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c976-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c976-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c976-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c976-108">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui avviare un failover.</span><span class="sxs-lookup"><span data-stu-id="6c976-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failover.</span></span>

</dd> <dt>

<span data-ttu-id="6c976-109">*SnapshotSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c976-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c976-110">Riferimento a un'istanza [**di \_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) che rappresenta lo snapshot utilizzato per il failover.</span><span class="sxs-lookup"><span data-stu-id="6c976-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used for the failover.</span></span> <span data-ttu-id="6c976-111">Se questo parametro è **null**, il failover deve essere eseguito fino al momento più recente.</span><span class="sxs-lookup"><span data-stu-id="6c976-111">If this parameter is **Null**, the failover is to be performed to the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="6c976-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="6c976-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c976-113">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6c976-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c976-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c976-114">Return value</span></span>

<span data-ttu-id="6c976-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6c976-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6c976-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="6c976-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="6c976-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="6c976-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="6c976-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="6c976-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="6c976-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="6c976-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="6c976-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-124">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="6c976-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="6c976-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="6c976-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="6c976-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="6c976-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="6c976-129">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="6c976-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6c976-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c976-130">Requirements</span></span>



| <span data-ttu-id="6c976-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c976-131">Requirement</span></span> | <span data-ttu-id="6c976-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6c976-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c976-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c976-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6c976-134">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6c976-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6c976-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c976-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6c976-136">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6c976-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6c976-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6c976-137">Namespace</span></span><br/>                | <span data-ttu-id="6c976-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6c976-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6c976-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6c976-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c976-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c976-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c976-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6c976-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c976-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6c976-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6c976-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c976-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c976-144">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="6c976-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="6c976-145">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="6c976-145">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="6c976-146">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="6c976-146">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

