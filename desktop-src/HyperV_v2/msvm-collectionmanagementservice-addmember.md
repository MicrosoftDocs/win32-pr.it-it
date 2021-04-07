---
description: Aggiunge l'elemento gestito specificato come membro dell'oggetto CollectionOfMSEs CIM specificato \_ .
ms.assetid: 6f23eecc-b445-4495-ae96-76b89652a1cb
title: Metodo AddMember della classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.AddMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6b885701086262fda48c5d50abd750eca6866c72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760499"
---
# <a name="addmember-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="c872f-103">Metodo AddMember della classe MSVM \_ CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="c872f-103">AddMember method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="c872f-104">Aggiunge l'elemento gestito specificato come membro dell'oggetto [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="c872f-104">Adds the specified managed element as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c872f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c872f-105">Syntax</span></span>


```mof
uint32 AddMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c872f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c872f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c872f-107">*Membro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c872f-107">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c872f-108">Membro da aggiungere alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="c872f-108">The member to add to the collection.</span></span>

</dd> <dt>

<span data-ttu-id="c872f-109">*Raccolta* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c872f-109">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c872f-110">Raccolta a cui aggiungere il membro.</span><span class="sxs-lookup"><span data-stu-id="c872f-110">The collection to add the member to.</span></span>

</dd> <dt>

<span data-ttu-id="c872f-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c872f-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c872f-112">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="c872f-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c872f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c872f-113">Return value</span></span>

<span data-ttu-id="c872f-114">Restituisce 0 se ha esito positivo oppure 4096 se il processo è stato avviato. in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="c872f-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c872f-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="c872f-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="c872f-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="c872f-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="c872f-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="c872f-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="c872f-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="c872f-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c872f-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-123">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c872f-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="c872f-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c872f-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="c872f-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c872f-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c872f-128">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="c872f-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c872f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c872f-129">Requirements</span></span>



| <span data-ttu-id="c872f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c872f-130">Requirement</span></span> | <span data-ttu-id="c872f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c872f-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c872f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c872f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c872f-133">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c872f-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c872f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c872f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c872f-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c872f-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c872f-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c872f-136">Namespace</span></span><br/>                | <span data-ttu-id="c872f-137">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c872f-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c872f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c872f-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c872f-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c872f-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c872f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c872f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c872f-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c872f-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c872f-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c872f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c872f-143">**\_CollectionManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="c872f-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




