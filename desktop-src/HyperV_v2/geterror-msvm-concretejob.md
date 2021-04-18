---
description: Recupera l'oggetto errore per il processo, se disponibile.
ms.assetid: 7E810CBE-F18F-4EFA-B52E-631CD071D136
title: Metodo GetError della classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 63279d8bc08f0b9f1955f694470a3744defd8054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307746"
---
# <a name="geterror-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="27cb7-103">Metodo GetError della \_ classe ConcreteJob di MSVM</span><span class="sxs-lookup"><span data-stu-id="27cb7-103">GetError method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="27cb7-104">Recupera l'oggetto errore per il processo, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="27cb7-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="27cb7-105">Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce un oggetto [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="27cb7-105">When the job is executing or has terminated without error, then this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="27cb7-106">Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, viene restituita un'istanza di **\_ errore CIM** .</span><span class="sxs-lookup"><span data-stu-id="27cb7-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="27cb7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27cb7-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="27cb7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="27cb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27cb7-109">*Errore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="27cb7-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27cb7-110">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="27cb7-110">Type: **string**</span></span>

<span data-ttu-id="27cb7-111">Se lo stato operativo del processo non è 2 (OK), questo metodo restituisce un'istanza incorporata della classe [**di \_ errore MSVM**](msvm-error.md) in formato CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="27cb7-111">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="27cb7-112">Se lo stato operativo del processo è 2 (OK), viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="27cb7-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27cb7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27cb7-113">Return value</span></span>

<span data-ttu-id="27cb7-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27cb7-114">Type: **uint32**</span></span>

<span data-ttu-id="27cb7-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="27cb7-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="27cb7-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="27cb7-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="27cb7-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="27cb7-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="27cb7-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="27cb7-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="27cb7-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="27cb7-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="27cb7-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="27cb7-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="27cb7-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="27cb7-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="27cb7-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="27cb7-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="27cb7-123">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="27cb7-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="27cb7-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="27cb7-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="27cb7-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="27cb7-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="27cb7-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="27cb7-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="27cb7-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="27cb7-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="27cb7-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="27cb7-128">Remarks</span></span>

<span data-ttu-id="27cb7-129">L'accesso alla [**classe \_ ConcreteJob di MSVM**](msvm-concretejob.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="27cb7-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="27cb7-130">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="27cb7-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="27cb7-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27cb7-131">Requirements</span></span>



| <span data-ttu-id="27cb7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="27cb7-132">Requirement</span></span> | <span data-ttu-id="27cb7-133">Valore</span><span class="sxs-lookup"><span data-stu-id="27cb7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27cb7-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27cb7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="27cb7-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="27cb7-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="27cb7-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27cb7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="27cb7-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="27cb7-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27cb7-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="27cb7-138">Namespace</span></span><br/>                | <span data-ttu-id="27cb7-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="27cb7-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="27cb7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="27cb7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27cb7-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27cb7-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="27cb7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="27cb7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27cb7-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="27cb7-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="27cb7-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27cb7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27cb7-145">**\_ConcreteJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="27cb7-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

