---
description: Avvia un'operazione di arresto del sistema operativo nella macchina virtuale figlio associata. Se viene restituito zero (0), l'arresto è stato avviato correttamente. Qualsiasi altro codice restituito indica una condizione di errore.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Metodo InitiateShutdown della classe Msvm_ShutdownComponent (winreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 266ab64bb058325ac165a2e12c2a91d442a90269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232267"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="299b6-105">Metodo InitiateShutdown della classe MSVM \_ ShutdownComponent</span><span class="sxs-lookup"><span data-stu-id="299b6-105">InitiateShutdown method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="299b6-106">Avvia un'operazione di arresto del sistema operativo nella macchina virtuale figlio associata.</span><span class="sxs-lookup"><span data-stu-id="299b6-106">Initiates an operating system shutdown operation on the associated child virtual machine.</span></span> <span data-ttu-id="299b6-107">Se viene restituito zero (0), l'arresto è stato avviato correttamente.</span><span class="sxs-lookup"><span data-stu-id="299b6-107">If zero (0) is returned, then the shutdown was initiated successfully.</span></span> <span data-ttu-id="299b6-108">Qualsiasi altro codice restituito indica una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="299b6-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="299b6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="299b6-109">Syntax</span></span>


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="299b6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="299b6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="299b6-111">*Forza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="299b6-111">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="299b6-112">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="299b6-112">Type: **boolean**</span></span>

<span data-ttu-id="299b6-113">Flag che, se **true**, impone la chiusura delle applicazioni nonostante i dati non salvati.</span><span class="sxs-lookup"><span data-stu-id="299b6-113">A flag which, if **True**, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="299b6-114">*Motivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="299b6-114">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="299b6-115">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="299b6-115">Type: **string**</span></span>

<span data-ttu-id="299b6-116">Motivo dell'operazione di arresto.</span><span class="sxs-lookup"><span data-stu-id="299b6-116">The reason for the shutdown operation.</span></span> <span data-ttu-id="299b6-117">Si tratta di una stringa definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="299b6-117">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="299b6-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="299b6-118">Return value</span></span>

<span data-ttu-id="299b6-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="299b6-119">Type: **uint32**</span></span>

<dl> <dt>

<span data-ttu-id="299b6-120">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="299b6-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-121">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="299b6-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-122">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="299b6-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-123">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="299b6-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-124">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="299b6-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-125">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="299b6-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-126">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="299b6-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-127">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="299b6-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-128">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="299b6-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-129">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="299b6-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-130">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="299b6-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-131">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="299b6-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-132">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="299b6-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-133">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="299b6-133">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-134">**Il sistema non è pronto** (32780)</span><span class="sxs-lookup"><span data-stu-id="299b6-134">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-135">**Il computer è bloccato e non può essere arrestato senza l'opzione Force** (32781)</span><span class="sxs-lookup"><span data-stu-id="299b6-135">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="299b6-136">**È in corso un arresto del sistema** (32782)</span><span class="sxs-lookup"><span data-stu-id="299b6-136">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="299b6-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="299b6-137">Remarks</span></span>

<span data-ttu-id="299b6-138">L'accesso alla [**classe \_ ShutdownComponent di MSVM**](msvm-shutdowncomponent.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="299b6-138">Access to the [**Msvm\_ShutdownComponent**](msvm-shutdowncomponent.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="299b6-139">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="299b6-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="299b6-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="299b6-140">Requirements</span></span>



| <span data-ttu-id="299b6-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="299b6-141">Requirement</span></span> | <span data-ttu-id="299b6-142">Valore</span><span class="sxs-lookup"><span data-stu-id="299b6-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="299b6-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="299b6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="299b6-144">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="299b6-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="299b6-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="299b6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="299b6-146">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="299b6-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="299b6-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="299b6-147">Namespace</span></span><br/>                | <span data-ttu-id="299b6-148">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="299b6-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="299b6-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="299b6-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="299b6-150"><dt>Winreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="299b6-150"><dt>Winreg.h</dt></span></span> </dl>                     |
| <span data-ttu-id="299b6-151">MOF</span><span class="sxs-lookup"><span data-stu-id="299b6-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="299b6-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="299b6-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="299b6-153">DLL</span><span class="sxs-lookup"><span data-stu-id="299b6-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="299b6-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="299b6-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="299b6-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="299b6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299b6-156">**\_ShutdownComponent MSVM**</span><span class="sxs-lookup"><span data-stu-id="299b6-156">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

