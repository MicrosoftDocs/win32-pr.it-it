---
description: 'IUserIdentityManager:: Logon non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'Metodo IUserIdentityManager:: Logon (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127830"
---
# <a name="iuseridentitymanagerlogon-method"></a><span data-ttu-id="93c8e-104">Metodo IUserIdentityManager:: Logon</span><span class="sxs-lookup"><span data-stu-id="93c8e-104">IUserIdentityManager::Logon method</span></span>

<span data-ttu-id="93c8e-105">\[**IUserIdentityManager:: Logon** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="93c8e-105">\[**IUserIdentityManager::Logon** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="93c8e-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="93c8e-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="93c8e-107">Visualizza un'interfaccia utente per l'utente, consentendo all'utente di scegliere un'identità utente.</span><span class="sxs-lookup"><span data-stu-id="93c8e-107">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="93c8e-108">Se l'esito è positivo, l'identità utente verrà registrata e recuperata.</span><span class="sxs-lookup"><span data-stu-id="93c8e-108">If successful, the user identity will be logged on and retrieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c8e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93c8e-109">Syntax</span></span>


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="93c8e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="93c8e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c8e-111">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93c8e-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93c8e-112">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="93c8e-112">Type: **HWND**</span></span>

<span data-ttu-id="93c8e-113">Valore **HWND** che identifica una finestra che verrà portata in primo piano dopo che l'interfaccia utente di accesso viene rilasciata.</span><span class="sxs-lookup"><span data-stu-id="93c8e-113">An **HWND** value that identifies a window that will be brought to the foreground after the logon UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="93c8e-114">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93c8e-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93c8e-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="93c8e-115">Type: **DWORD**</span></span>

<span data-ttu-id="93c8e-116">Flag facoltativi per definire il comportamento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="93c8e-116">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="93c8e-117">Impostare su UIL \_ Force \_ UI per forzare la visualizzazione dell'interfaccia utente, anche se è già stata scelta un'identità.</span><span class="sxs-lookup"><span data-stu-id="93c8e-117">Set to UIL\_FORCE\_UI to force the UI to display, even if an identity has already been chosen.</span></span>

</dd> <dt>

<span data-ttu-id="93c8e-118">*ppIdentity* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="93c8e-118">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93c8e-119">Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="93c8e-119">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="93c8e-120">Indirizzo del puntatore che riceve l'identità utente scelta.</span><span class="sxs-lookup"><span data-stu-id="93c8e-120">The address of the pointer that receives the chosen user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c8e-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93c8e-121">Return value</span></span>

<span data-ttu-id="93c8e-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="93c8e-122">Type: **HRESULT**</span></span>

<span data-ttu-id="93c8e-123">Risultato dell'operazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="93c8e-123">Result of the logon operation.</span></span> <span data-ttu-id="93c8e-124">Se ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93c8e-124">If successful, it returns S\_OK.</span></span> <span data-ttu-id="93c8e-125">In caso contrario, verrà restituito uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="93c8e-125">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="93c8e-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="93c8e-126">Return code</span></span>                                                                                            | <span data-ttu-id="93c8e-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93c8e-127">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93c8e-128"><dt>**E \_ utente \_ annullato**</dt></span><span class="sxs-lookup"><span data-stu-id="93c8e-128"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="93c8e-129">L'utente ha annullato l'operazione di accesso dall'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="93c8e-129">The user canceled the logon operation from the UI.</span></span><br/>                               |
| <dl> <span data-ttu-id="93c8e-130"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="93c8e-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="93c8e-131">Non è stato possibile creare l'identità utente.</span><span class="sxs-lookup"><span data-stu-id="93c8e-131">The user identity could not be created.</span></span><br/>                                          |
| <dl> <span data-ttu-id="93c8e-132"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="93c8e-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="93c8e-133">L'operazione non è riuscita in modo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="93c8e-133">The operation failed unexpectedly.</span></span><br/>                                               |
| <dl> <span data-ttu-id="93c8e-134"><dt>**\_identità E \_ disabilitate**</dt></span><span class="sxs-lookup"><span data-stu-id="93c8e-134"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="93c8e-135">Gestione identità è disabilitato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="93c8e-135">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="93c8e-136"><dt>**\_identità \_ disabilitate**</dt></span><span class="sxs-lookup"><span data-stu-id="93c8e-136"><dt>**S\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="93c8e-137">Gestione identità è disabilitato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="93c8e-137">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="93c8e-138"><dt>**\_modifica dell'identità E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="93c8e-138"><dt>**E\_IDENTITY\_CHANGING**</dt></span></span> </dl>   | <span data-ttu-id="93c8e-139">Il sistema sta attualmente cambiando identità e non è in grado di completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="93c8e-139">The system is currently switching identities, and cannot complete the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="93c8e-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93c8e-140">Requirements</span></span>



| <span data-ttu-id="93c8e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="93c8e-141">Requirement</span></span> | <span data-ttu-id="93c8e-142">Valore</span><span class="sxs-lookup"><span data-stu-id="93c8e-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93c8e-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c8e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="93c8e-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="93c8e-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="93c8e-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c8e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="93c8e-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="93c8e-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="93c8e-147">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="93c8e-147">End of client support</span></span><br/>    | <span data-ttu-id="93c8e-148">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="93c8e-148">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="93c8e-149">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="93c8e-149">End of server support</span></span><br/>    | <span data-ttu-id="93c8e-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="93c8e-150">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="93c8e-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93c8e-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="93c8e-152"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="93c8e-152"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="93c8e-153">IDL</span><span class="sxs-lookup"><span data-stu-id="93c8e-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93c8e-154"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93c8e-154"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="93c8e-155">DLL</span><span class="sxs-lookup"><span data-stu-id="93c8e-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93c8e-156"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93c8e-156"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93c8e-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93c8e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c8e-158">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="93c8e-158">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="93c8e-159">**IUserIdentityManager:: disconnessione**</span><span class="sxs-lookup"><span data-stu-id="93c8e-159">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> <dt>

[<span data-ttu-id="93c8e-160">**IUserIdentityManager::ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="93c8e-160">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




