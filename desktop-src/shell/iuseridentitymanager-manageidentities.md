---
description: 'IUserIdentityManager:: ManageIdentities non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'Metodo IUserIdentityManager:: ManageIdentities (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342436"
---
# <a name="iuseridentitymanagermanageidentities-method"></a><span data-ttu-id="b5c1c-104">Metodo IUserIdentityManager:: ManageIdentities</span><span class="sxs-lookup"><span data-stu-id="b5c1c-104">IUserIdentityManager::ManageIdentities method</span></span>

<span data-ttu-id="b5c1c-105">\[**IUserIdentityManager:: ManageIdentities** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="b5c1c-105">\[**IUserIdentityManager::ManageIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="b5c1c-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="b5c1c-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="b5c1c-107">Visualizza un'interfaccia utente per l'utente, consentendo all'utente di gestire le identità utente.</span><span class="sxs-lookup"><span data-stu-id="b5c1c-107">Displays a UI to the user, allowing the user to manage user identities.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c1c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5c1c-108">Syntax</span></span>


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b5c1c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5c1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5c1c-110">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5c1c-110">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c1c-111">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="b5c1c-111">Type: **HWND**</span></span>

<span data-ttu-id="b5c1c-112">Valore **HWND** che identifica una finestra che verrà portata in primo piano dopo la chiusura dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b5c1c-112">An **HWND** value that identifies a window that will be brought to the foreground after the UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="b5c1c-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5c1c-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c1c-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b5c1c-114">Type: **DWORD**</span></span>

<span data-ttu-id="b5c1c-115">Flag facoltativi per definire il comportamento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b5c1c-115">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="b5c1c-116">Impostare su UIMI \_ Crea \_ nuova \_ identità per richiedere all'utente di creare una nuova identità.</span><span class="sxs-lookup"><span data-stu-id="b5c1c-116">Set to UIMI\_CREATE\_NEW\_IDENTITY to prompt the user to create a new identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5c1c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5c1c-117">Return value</span></span>

<span data-ttu-id="b5c1c-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b5c1c-118">Type: **HRESULT**</span></span>

<span data-ttu-id="b5c1c-119">Risultato dell'operazione di gestione.</span><span class="sxs-lookup"><span data-stu-id="b5c1c-119">The result of the management operation.</span></span> <span data-ttu-id="b5c1c-120">Se ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5c1c-120">If successful, it returns S\_OK.</span></span> <span data-ttu-id="b5c1c-121">In caso contrario, verrà restituito uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="b5c1c-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="b5c1c-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b5c1c-122">Return code</span></span>                                                                                            | <span data-ttu-id="b5c1c-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5c1c-123">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="b5c1c-124"><dt>**\_identità E \_ disabilitate**</dt></span><span class="sxs-lookup"><span data-stu-id="b5c1c-124"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="b5c1c-125">Gestione identità è disabilitato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b5c1c-125">Identity management is disabled on the system.</span></span><br/> |
| <dl> <span data-ttu-id="b5c1c-126"><dt>**E \_ utente \_ annullato**</dt></span><span class="sxs-lookup"><span data-stu-id="b5c1c-126"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="b5c1c-127">L'utente ha annullato la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b5c1c-127">The user canceled the dialog.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="b5c1c-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5c1c-128">Requirements</span></span>



| <span data-ttu-id="b5c1c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5c1c-129">Requirement</span></span> | <span data-ttu-id="b5c1c-130">Valore</span><span class="sxs-lookup"><span data-stu-id="b5c1c-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c1c-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5c1c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b5c1c-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5c1c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b5c1c-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5c1c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b5c1c-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5c1c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b5c1c-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b5c1c-135">End of client support</span></span><br/>    | <span data-ttu-id="b5c1c-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b5c1c-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b5c1c-137">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b5c1c-137">End of server support</span></span><br/>    | <span data-ttu-id="b5c1c-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5c1c-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b5c1c-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5c1c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5c1c-140"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5c1c-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5c1c-141">IDL</span><span class="sxs-lookup"><span data-stu-id="b5c1c-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5c1c-142"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5c1c-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="b5c1c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b5c1c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5c1c-144"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5c1c-144"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c1c-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5c1c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c1c-146">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="b5c1c-146">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="b5c1c-147">**IUserIdentityManager:: Logon**</span><span class="sxs-lookup"><span data-stu-id="b5c1c-147">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="b5c1c-148">**IUserIdentityManager:: disconnessione**</span><span class="sxs-lookup"><span data-stu-id="b5c1c-148">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




