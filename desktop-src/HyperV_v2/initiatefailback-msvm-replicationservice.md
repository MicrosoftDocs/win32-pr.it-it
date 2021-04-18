---
description: Avvia il failback per una macchina virtuale di ripristino.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: 'Metodo Msvm_ReplicationService:: InitiateFailback'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b356982296427212287ea11b528a7878dc166245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309512"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a><span data-ttu-id="fc5cd-103">\_Metodo MSVM ReplicationService:: InitiateFailback</span><span class="sxs-lookup"><span data-stu-id="fc5cd-103">Msvm\_ReplicationService::InitiateFailback method</span></span>

<span data-ttu-id="fc5cd-104">Avvia il failback per una macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-104">Initiates the failback for a recovery virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc5cd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc5cd-105">Syntax</span></span>


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="fc5cd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc5cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc5cd-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc5cd-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5cd-108">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui avviare un failback.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failback.</span></span>

</dd> <dt>

<span data-ttu-id="fc5cd-109">*ReplicationSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc5cd-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5cd-110">Rappresentazione di stringa di un'istanza incorporata della classe [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) che definisce le impostazioni di replica per il failback.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-110">A string representation of an embedded instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the failback.</span></span>

</dd> <dt>

<span data-ttu-id="fc5cd-111">*RecoveryPointIdentifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc5cd-111">*RecoveryPointIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5cd-112">Input facoltativo che identifica il punto di ripristino a cui viene richiesto il failback.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-112">Optional input that identifies the recovery point to which failback is requested.</span></span>

</dd> <dt>

<span data-ttu-id="fc5cd-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="fc5cd-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc5cd-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc5cd-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="fc5cd-115">Questo riferimento può essere usato per monitorare lo stato di avanzamento e per ottenere il risultato del metodo.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-115">This reference can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc5cd-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc5cd-116">Return value</span></span>

<span data-ttu-id="fc5cd-117">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fc5cd-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-119">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-123">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-125">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-126">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-127">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-128">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-129">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fc5cd-131">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="fc5cd-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="fc5cd-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc5cd-132">Remarks</span></span>

<span data-ttu-id="fc5cd-133">**InitiateFailback** funziona in una macchina virtuale di ripristino e porta la macchina virtuale allo stato *WaitingForFailback* .</span><span class="sxs-lookup"><span data-stu-id="fc5cd-133">**InitiateFailback** works on a recovery virtual machine and takes the virtual machine to *WaitingForFailback* state.</span></span> <span data-ttu-id="fc5cd-134">**InitiateFailback** consente di eseguire il reverse della richiesta di failback al provider corrispondente, che consente di risincronizzare il punto di ripristino dal lato nuovo-primario.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-134">**InitiateFailback** forwards the failback request to the corresponding provider, which reverse-resyncs the recovery point from new-primary side.</span></span> <span data-ttu-id="fc5cd-135">Al termine del failback del punto di ripristino richiesto, lo stato di replica passa allo stato *FailbackCompleted* .</span><span class="sxs-lookup"><span data-stu-id="fc5cd-135">After failback of the requested recovery point completes, the replication state moves to *FailbackCompleted* state.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc5cd-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc5cd-136">Requirements</span></span>



| <span data-ttu-id="fc5cd-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc5cd-137">Requirement</span></span> | <span data-ttu-id="fc5cd-138">Valore</span><span class="sxs-lookup"><span data-stu-id="fc5cd-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc5cd-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc5cd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fc5cd-140">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fc5cd-140">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="fc5cd-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc5cd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fc5cd-142">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc5cd-142">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fc5cd-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fc5cd-143">Namespace</span></span><br/>                | <span data-ttu-id="fc5cd-144">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fc5cd-144">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="fc5cd-145">MOF</span><span class="sxs-lookup"><span data-stu-id="fc5cd-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc5cd-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc5cd-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc5cd-147">DLL</span><span class="sxs-lookup"><span data-stu-id="fc5cd-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc5cd-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc5cd-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc5cd-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc5cd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc5cd-150">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="fc5cd-150">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

