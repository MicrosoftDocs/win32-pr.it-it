---
description: Rimuove un computer da un dominio o un gruppo di lavoro.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Metodo UnjoinDomainOrWorkgroup della classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878245"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="c2a2b-103">Metodo UnjoinDomainOrWorkgroup della \_ classe ComputerSystem Win32</span><span class="sxs-lookup"><span data-stu-id="c2a2b-103">UnjoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="c2a2b-104">Il metodo **UnjoinDomainOrWorkgroup** rimuove un computer da un dominio o un gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-104">The **UnjoinDomainOrWorkgroup** method removes a computer system from a domain or workgroup.</span></span>

<span data-ttu-id="c2a2b-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c2a2b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c2a2b-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c2a2b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a2b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2a2b-107">Syntax</span></span>


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="c2a2b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2a2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a2b-109">*Password* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c2a2b-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2a2b-110">Se il parametro *username* specifica un nome di account, il parametro *password* deve puntare alla password da usare per la connessione al controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-110">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="c2a2b-111">In caso contrario, questo parametro deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-111">Otherwise, this parameter must be **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="c2a2b-112">Per la connessione a winmgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) sul puntatore [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) , la *password* deve usare un livello di autenticazione elevato, non inferiore alla **\_ \_ \_ \_ \_ privacy PKT del livello auth C**.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-112">*Password* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="c2a2b-113">Se da locale a winmgmt, questo non rappresenta un problema.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-113">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="c2a2b-114">*Nome utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2a2b-114">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2a2b-115">Puntatore a una stringa di caratteri con terminazione null costante che specifica il nome dell'account da utilizzare per la connessione al controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-115">Pointer to a constant null-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="c2a2b-116">È necessario specificare un dominio e un account utente, ad esempio "dominio \\ utente" o " user@domain ".</span><span class="sxs-lookup"><span data-stu-id="c2a2b-116">Must specify a domain and user account, for example, "domain\\user" or "user@domain".</span></span> <span data-ttu-id="c2a2b-117">Se questo parametro è **null**, viene utilizzato il contesto del chiamante.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-117">If this parameter is **NULL**, the caller context is used.</span></span>

> [!Note]  
> <span data-ttu-id="c2a2b-118">Il *nome utente* deve usare un livello di autenticazione elevato, non inferiore alla **\_ \_ \_ \_ \_ privacy PKT del livello auth C**, quando si connette a winmgmt o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) sul puntatore [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="c2a2b-118">*UserName* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="c2a2b-119">Se da locale a winmgmt, questo non rappresenta un problema.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-119">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="c2a2b-120">*FUnjoinOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2a2b-120">*FUnjoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2a2b-121">Set di flag di bit che definiscono le opzioni di Unjoin.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-121">Set of bit flags defining the unjoin options.</span></span>

<dt>



 <span data-ttu-id="c2a2b-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="c2a2b-122">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c2a2b-123">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-123">Default.</span></span> <span data-ttu-id="c2a2b-124">Nessuna opzione.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-124">No options.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span data-ttu-id="c2a2b-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**Netsetup \_ \_Eliminazione Acct** (4)</span><span class="sxs-lookup"><span data-stu-id="c2a2b-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP\_ACCT\_DELETE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c2a2b-126">Disabilitare l'account Active Directory dopo l'operazione di Unjoin, ma non eliminare l'account.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-126">Disable the Active Directory account after the unjoin operation, but do not delete the account.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a2b-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2a2b-127">Return value</span></span>

<span data-ttu-id="c2a2b-128">Il metodo **UnjoinDomainOrWorkgroup** restituisce 0 (zero) in caso di esito positivo o se non è presente alcuna opzione.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-128">The **UnjoinDomainOrWorkgroup** method returns 0 (zero) on success or when no options are involved.</span></span> <span data-ttu-id="c2a2b-129">Qualsiasi altro valore indica un errore.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-129">Any other value indicates an error.</span></span> <span data-ttu-id="c2a2b-130">Per i codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c2a2b-130">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c2a2b-131">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c2a2b-131">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c2a2b-132">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="c2a2b-132">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c2a2b-133">**Altro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="c2a2b-133">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c2a2b-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2a2b-134">Remarks</span></span>

<span data-ttu-id="c2a2b-135">Dopo aver chiamato questo metodo, riavviare il computer interessato per applicare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-135">After calling this method, restart the affected computer to apply the changes.</span></span>

## <a name="examples"></a><span data-ttu-id="c2a2b-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="c2a2b-136">Examples</span></span>

<span data-ttu-id="c2a2b-137">[Separare un computer da un dominio](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) L'esempio VBScript consente di separare il computer locale dal dominio corrente e di disabilitare l'account del computer.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-137">[The Unjoin a Computer from a Domain](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) VBScript sample unjoins the local computer from its current domain and disables the computer account.</span></span>

<span data-ttu-id="c2a2b-138">L'esempio di [Unjoin a computer da un dominio che utilizza lo script vbs](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) è un join di un computer specificato da un dominio.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-138">The [Unjoin a Computer from a Domain using VBS script](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) sample unjoins a specified computer from a domain.</span></span> <span data-ttu-id="c2a2b-139">.</span><span class="sxs-lookup"><span data-stu-id="c2a2b-139">.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a2b-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2a2b-140">Requirements</span></span>



| <span data-ttu-id="c2a2b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2a2b-141">Requirement</span></span> | <span data-ttu-id="c2a2b-142">Valore</span><span class="sxs-lookup"><span data-stu-id="c2a2b-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a2b-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2a2b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a2b-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2a2b-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2a2b-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2a2b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a2b-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2a2b-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2a2b-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c2a2b-147">Namespace</span></span><br/>                | <span data-ttu-id="c2a2b-148">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c2a2b-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c2a2b-149">MOF</span><span class="sxs-lookup"><span data-stu-id="c2a2b-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2a2b-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2a2b-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2a2b-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c2a2b-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2a2b-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2a2b-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2a2b-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2a2b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a2b-154">**\_ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="c2a2b-154">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="c2a2b-155">**Metodo JoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="c2a2b-155">**JoinDomainOrWorkgroup method**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

