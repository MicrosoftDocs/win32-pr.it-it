---
description: Rimuove uno snapshot esistente e tutti i relativi elementi figlio di una macchina virtuale.
ms.assetid: d7a6442a-41a5-4e82-8ec8-dbc8e14d9a89
title: Metodo DestroySnapshotTree della classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshotTree
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5658e954766531765c47f8bef80d5509f2ad27c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315511"
---
# <a name="destroysnapshottree-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="ebfec-103">Metodo DestroySnapshotTree della classe MSVM \_ VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="ebfec-103">DestroySnapshotTree method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="ebfec-104">Rimuove uno snapshot esistente e tutti i relativi elementi figlio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ebfec-104">Removes an existing snapshot, and all its children, of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebfec-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebfec-105">Syntax</span></span>


```mof
uint32 DestroySnapshotTree(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ebfec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebfec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebfec-107">*SnapshotSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebfec-107">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebfec-108">Riferimento [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) che rappresenta l'albero di snapshot della macchina virtuale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ebfec-108">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot tree to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="ebfec-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ebfec-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebfec-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ebfec-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebfec-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebfec-111">Return value</span></span>

<span data-ttu-id="ebfec-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ebfec-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ebfec-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ebfec-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="ebfec-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="ebfec-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="ebfec-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="ebfec-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="ebfec-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ebfec-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ebfec-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ebfec-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="ebfec-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ebfec-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="ebfec-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ebfec-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ebfec-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ebfec-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebfec-126">Requirements</span></span>



| <span data-ttu-id="ebfec-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebfec-127">Requirement</span></span> | <span data-ttu-id="ebfec-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ebfec-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebfec-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebfec-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ebfec-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ebfec-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ebfec-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebfec-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ebfec-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ebfec-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ebfec-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ebfec-133">Namespace</span></span><br/>                | <span data-ttu-id="ebfec-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ebfec-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ebfec-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ebfec-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebfec-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebfec-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebfec-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ebfec-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebfec-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ebfec-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ebfec-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebfec-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebfec-140">**\_VirtualSystemSnapshotService MSVM**</span><span class="sxs-lookup"><span data-stu-id="ebfec-140">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="ebfec-141">**RemoveVirtualSystemSnapshotTree (V1)**</span><span class="sxs-lookup"><span data-stu-id="ebfec-141">**RemoveVirtualSystemSnapshotTree (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshottree-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

