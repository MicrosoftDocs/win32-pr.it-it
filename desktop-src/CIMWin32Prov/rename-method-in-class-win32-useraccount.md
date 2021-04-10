---
description: Rinomina un nome di account utente.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Rinominare il metodo della classe Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127363"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a><span data-ttu-id="60be8-103">Rinominare il metodo della \_ classe Win32 AccountUtente</span><span class="sxs-lookup"><span data-stu-id="60be8-103">Rename method of the Win32\_UserAccount class</span></span>

<span data-ttu-id="60be8-104">Il metodo **Rinomina** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) Rinomina un nome di account utente.</span><span class="sxs-lookup"><span data-stu-id="60be8-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a user account name.</span></span>

<span data-ttu-id="60be8-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="60be8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="60be8-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="60be8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="60be8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60be8-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="60be8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="60be8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60be8-109">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60be8-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60be8-110">Nome del nuovo account.</span><span class="sxs-lookup"><span data-stu-id="60be8-110">New account name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60be8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60be8-111">Return value</span></span>

<span data-ttu-id="60be8-112">Restituisce uno dei valori elencati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="60be8-112">Returns one of the values listed in the following list.</span></span> <span data-ttu-id="60be8-113">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="60be8-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="60be8-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="60be8-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="60be8-115">**Success**</span><span class="sxs-lookup"><span data-stu-id="60be8-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="60be8-116">0</span><span class="sxs-lookup"><span data-stu-id="60be8-116">0</span></span>

<span data-ttu-id="60be8-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="60be8-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="60be8-118">**Istanza non trovata**</span><span class="sxs-lookup"><span data-stu-id="60be8-118">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="60be8-119">1</span><span class="sxs-lookup"><span data-stu-id="60be8-119">1</span></span>

<span data-ttu-id="60be8-120">Istanza non trovata.</span><span class="sxs-lookup"><span data-stu-id="60be8-120">Instance not found.</span></span>

</dd> <dt>

<span data-ttu-id="60be8-121">**Istanza obbligatoria**</span><span class="sxs-lookup"><span data-stu-id="60be8-121">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="60be8-122">2</span><span class="sxs-lookup"><span data-stu-id="60be8-122">2</span></span>

<span data-ttu-id="60be8-123">Istanza richiesta.</span><span class="sxs-lookup"><span data-stu-id="60be8-123">Instance required.</span></span>

</dd> <dt>

<span data-ttu-id="60be8-124">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="60be8-124">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="60be8-125">3</span><span class="sxs-lookup"><span data-stu-id="60be8-125">3</span></span>

<span data-ttu-id="60be8-126">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="60be8-126">Invalid parameter.</span></span>

</dd> <dt>

<span data-ttu-id="60be8-127">**Utente non trovato**</span><span class="sxs-lookup"><span data-stu-id="60be8-127">**User not found**</span></span>
</dt> <dd>

<span data-ttu-id="60be8-128">4</span><span class="sxs-lookup"><span data-stu-id="60be8-128">4</span></span>

<span data-ttu-id="60be8-129">Utente non trovato.</span><span class="sxs-lookup"><span data-stu-id="60be8-129">User not found.</span></span>

</dd> <dt>

<span data-ttu-id="60be8-130">**Dominio non trovato**</span><span class="sxs-lookup"><span data-stu-id="60be8-130">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="60be8-131">5</span><span class="sxs-lookup"><span data-stu-id="60be8-131">5</span></span>

<span data-ttu-id="60be8-132">Il dominio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="60be8-132">Domain not found.</span></span>

</dd> <dt>

<span data-ttu-id="60be8-133">**L'operazione è consentita solo sul controller di dominio primario del dominio**</span><span class="sxs-lookup"><span data-stu-id="60be8-133">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="60be8-134">6</span><span class="sxs-lookup"><span data-stu-id="60be8-134">6</span></span>

<span data-ttu-id="60be8-135">L'operazione è consentita solo sul controller di dominio primario del dominio.</span><span class="sxs-lookup"><span data-stu-id="60be8-135">Operation is allowed only on the primary domain controller of the domain.</span></span>

</dd> <dt>

<span data-ttu-id="60be8-136">**Operazione non consentita per l'ultimo account amministrativo.**</span><span class="sxs-lookup"><span data-stu-id="60be8-136">**Operation is not allowed on the last administrative account.**</span></span>
</dt> <dd>

<span data-ttu-id="60be8-137">7</span><span class="sxs-lookup"><span data-stu-id="60be8-137">7</span></span>

</dd> <dt>

<span data-ttu-id="60be8-138">**Operazione non consentita per gruppi speciali specificati. utente, amministratore, locale o Guest.**</span><span class="sxs-lookup"><span data-stu-id="60be8-138">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="60be8-139">8</span><span class="sxs-lookup"><span data-stu-id="60be8-139">8</span></span>

<span data-ttu-id="60be8-140">Operazione non consentita per gruppi speciali specificati: utente, amministratore, locale o Guest.</span><span class="sxs-lookup"><span data-stu-id="60be8-140">Operation is not allowed on specified special groups: user, admin, local, or guest.</span></span>

</dd> <dt>

<span data-ttu-id="60be8-141">**Altro errore API**</span><span class="sxs-lookup"><span data-stu-id="60be8-141">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="60be8-142">9</span><span class="sxs-lookup"><span data-stu-id="60be8-142">9</span></span>

<span data-ttu-id="60be8-143">Altro errore dell'API.</span><span class="sxs-lookup"><span data-stu-id="60be8-143">Other API error.</span></span>

</dd> <dt>

<span data-ttu-id="60be8-144">**Errore interno**</span><span class="sxs-lookup"><span data-stu-id="60be8-144">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="60be8-145">10</span><span class="sxs-lookup"><span data-stu-id="60be8-145">10</span></span>

<span data-ttu-id="60be8-146">Errore interno.</span><span class="sxs-lookup"><span data-stu-id="60be8-146">Internal error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60be8-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="60be8-147">Remarks</span></span>

<span data-ttu-id="60be8-148">Questa funzionalità viene implementata come metodo per fornire un contesto separato per il nuovo nome che è distinguibile dal valore della proprietà chiave per il nome associato all'istanza da modificare.</span><span class="sxs-lookup"><span data-stu-id="60be8-148">This functionality is implemented as a method to provide a separate context for the new name that is distinguishable from the key property value for Name that is associated with the instance to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="60be8-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60be8-149">Requirements</span></span>



| <span data-ttu-id="60be8-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="60be8-150">Requirement</span></span> | <span data-ttu-id="60be8-151">Valore</span><span class="sxs-lookup"><span data-stu-id="60be8-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60be8-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60be8-152">Minimum supported client</span></span><br/> | <span data-ttu-id="60be8-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60be8-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60be8-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60be8-154">Minimum supported server</span></span><br/> | <span data-ttu-id="60be8-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60be8-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60be8-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="60be8-156">Namespace</span></span><br/>                | <span data-ttu-id="60be8-157">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="60be8-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60be8-158">MOF</span><span class="sxs-lookup"><span data-stu-id="60be8-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60be8-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60be8-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60be8-160">DLL</span><span class="sxs-lookup"><span data-stu-id="60be8-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60be8-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60be8-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60be8-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60be8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60be8-163">**\_AccountUtente Win32**</span><span class="sxs-lookup"><span data-stu-id="60be8-163">**Win32\_UserAccount**</span></span>](win32-useraccount.md)
</dt> <dt>

<span data-ttu-id="60be8-164">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="60be8-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

