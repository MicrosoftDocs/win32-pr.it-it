---
description: Avvia un'operazione di riavvio del sistema operativo sulla macchina virtuale figlio associata.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Metodo InitiateReboot della classe Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 527569e8a5d6c2bb0a54294637ae19c13f5e3af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308205"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="3beaa-103">Metodo InitiateReboot della classe MSVM \_ ShutdownComponent</span><span class="sxs-lookup"><span data-stu-id="3beaa-103">InitiateReboot method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="3beaa-104">Avvia un'operazione di riavvio del sistema operativo sulla macchina virtuale figlio associata.</span><span class="sxs-lookup"><span data-stu-id="3beaa-104">Initiates an operating system reboot operation on the associated child virtual machine.</span></span>

<span data-ttu-id="3beaa-105">Se viene restituito zero (0), il riavvio è stato avviato correttamente.</span><span class="sxs-lookup"><span data-stu-id="3beaa-105">If zero (0) is returned, then the reboot was initiated successfully.</span></span> <span data-ttu-id="3beaa-106">Qualsiasi altro codice restituito indica una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="3beaa-106">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="3beaa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3beaa-107">Syntax</span></span>


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="3beaa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3beaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3beaa-109">*Forza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3beaa-109">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3beaa-110">Flag che, se TRUE, impone la chiusura delle applicazioni nonostante i dati non salvati.</span><span class="sxs-lookup"><span data-stu-id="3beaa-110">A flag which, if TRUE, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="3beaa-111">*Motivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3beaa-111">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3beaa-112">Motivo dell'operazione di riavvio.</span><span class="sxs-lookup"><span data-stu-id="3beaa-112">The reason for the reboot operation.</span></span> <span data-ttu-id="3beaa-113">Si tratta di una stringa definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3beaa-113">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3beaa-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3beaa-114">Return value</span></span>

<span data-ttu-id="3beaa-115">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3beaa-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="3beaa-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="3beaa-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="3beaa-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="3beaa-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="3beaa-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="3beaa-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="3beaa-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3beaa-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3beaa-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-124">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3beaa-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="3beaa-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3beaa-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="3beaa-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3beaa-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-129">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="3beaa-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-130">**Il sistema non è pronto** (32780)</span><span class="sxs-lookup"><span data-stu-id="3beaa-130">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-131">**Il computer è bloccato e non può essere arrestato senza l'opzione Force** (32781)</span><span class="sxs-lookup"><span data-stu-id="3beaa-131">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="3beaa-132">**È in corso un arresto del sistema** (32782)</span><span class="sxs-lookup"><span data-stu-id="3beaa-132">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3beaa-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3beaa-133">Requirements</span></span>



| <span data-ttu-id="3beaa-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3beaa-134">Requirement</span></span> | <span data-ttu-id="3beaa-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3beaa-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3beaa-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3beaa-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3beaa-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3beaa-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3beaa-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3beaa-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3beaa-139">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3beaa-139">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3beaa-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3beaa-140">Namespace</span></span><br/>                | <span data-ttu-id="3beaa-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3beaa-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3beaa-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3beaa-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3beaa-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3beaa-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3beaa-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3beaa-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3beaa-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3beaa-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3beaa-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3beaa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3beaa-147">**\_ShutdownComponent MSVM**</span><span class="sxs-lookup"><span data-stu-id="3beaa-147">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




