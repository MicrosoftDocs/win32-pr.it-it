---
description: Cancella lo stato di salvataggio da uno snapshot esistente.
ms.assetid: abb0ed4a-7f89-4d32-93d2-7491d2f2aa83
title: Metodo ClearSnapshotState della classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ClearSnapshotState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a218b600e45d91d8c744d6b49afe97666ddb51ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313375"
---
# <a name="clearsnapshotstate-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="12d00-103">Metodo ClearSnapshotState della classe MSVM \_ VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="12d00-103">ClearSnapshotState method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="12d00-104">Cancella lo stato di salvataggio da uno snapshot esistente.</span><span class="sxs-lookup"><span data-stu-id="12d00-104">Clears save state from an existing snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d00-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12d00-105">Syntax</span></span>


```mof
uint32 ClearSnapshotState(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="12d00-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12d00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12d00-107">*SnapshotSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12d00-107">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d00-108">Riferimento all'istanza di [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) che rappresenta lo snapshot il cui stato deve essere cancellato.</span><span class="sxs-lookup"><span data-stu-id="12d00-108">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot whose state is to be cleared.</span></span>

</dd> <dt>

<span data-ttu-id="12d00-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="12d00-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12d00-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="12d00-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12d00-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12d00-111">Return value</span></span>

<span data-ttu-id="12d00-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="12d00-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="12d00-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="12d00-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="12d00-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="12d00-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="12d00-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="12d00-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="12d00-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="12d00-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="12d00-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="12d00-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="12d00-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="12d00-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="12d00-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="12d00-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="12d00-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="12d00-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12d00-126">Requirements</span></span>



| <span data-ttu-id="12d00-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="12d00-127">Requirement</span></span> | <span data-ttu-id="12d00-128">Valore</span><span class="sxs-lookup"><span data-stu-id="12d00-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12d00-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12d00-129">Minimum supported client</span></span><br/> | <span data-ttu-id="12d00-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="12d00-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="12d00-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12d00-131">Minimum supported server</span></span><br/> | <span data-ttu-id="12d00-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="12d00-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12d00-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="12d00-133">Namespace</span></span><br/>                | <span data-ttu-id="12d00-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="12d00-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="12d00-135">MOF</span><span class="sxs-lookup"><span data-stu-id="12d00-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12d00-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12d00-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12d00-137">DLL</span><span class="sxs-lookup"><span data-stu-id="12d00-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12d00-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12d00-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="12d00-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12d00-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d00-140">**\_VirtualSystemSnapshotService MSVM**</span><span class="sxs-lookup"><span data-stu-id="12d00-140">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

