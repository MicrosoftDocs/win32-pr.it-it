---
description: Recupera l'oggetto errore per il processo di migrazione, se disponibile.
ms.assetid: 83a68ded-086a-42d9-b76d-e46af70d9b43
title: Metodo GetError della classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6dce1cb3728c854b1dac742099a3ca035d4865a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307744"
---
# <a name="geterror-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="fed87-103">Metodo GetError della \_ classe MigrationJob di MSVM</span><span class="sxs-lookup"><span data-stu-id="fed87-103">GetError method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="fed87-104">Recupera l'oggetto errore per il processo di migrazione, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="fed87-104">Retrieves the error object for the migration job, if one exists.</span></span> <span data-ttu-id="fed87-105">Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce un oggetto [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fed87-105">When the job is executing or has terminated without error, then this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="fed87-106">Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, viene restituita un'istanza di **\_ errore CIM** .</span><span class="sxs-lookup"><span data-stu-id="fed87-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="fed87-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fed87-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="fed87-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fed87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fed87-109">*Errore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fed87-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fed87-110">Se lo stato operativo del processo non è 2 (OK), questo metodo restituisce un'istanza incorporata della classe [**di \_ errore MSVM**](msvm-error.md) in formato CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="fed87-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="fed87-111">Se lo stato operativo del processo è 2 (OK), viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="fed87-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fed87-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fed87-112">Return value</span></span>

<span data-ttu-id="fed87-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fed87-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fed87-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="fed87-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fed87-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="fed87-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fed87-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="fed87-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fed87-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="fed87-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fed87-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="fed87-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fed87-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="fed87-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fed87-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="fed87-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fed87-121">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="fed87-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fed87-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="fed87-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fed87-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="fed87-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fed87-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="fed87-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fed87-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="fed87-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fed87-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fed87-126">Requirements</span></span>



| <span data-ttu-id="fed87-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fed87-127">Requirement</span></span> | <span data-ttu-id="fed87-128">Valore</span><span class="sxs-lookup"><span data-stu-id="fed87-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed87-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fed87-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fed87-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fed87-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fed87-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fed87-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fed87-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fed87-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fed87-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fed87-133">Namespace</span></span><br/>                | <span data-ttu-id="fed87-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fed87-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fed87-135">MOF</span><span class="sxs-lookup"><span data-stu-id="fed87-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fed87-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fed87-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fed87-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fed87-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fed87-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fed87-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fed87-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fed87-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed87-140">**\_MigrationJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="fed87-140">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

