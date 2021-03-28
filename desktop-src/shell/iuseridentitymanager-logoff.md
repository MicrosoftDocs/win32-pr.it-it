---
description: La disconnessione non è supportata e può essere modificata o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: 'Metodo IUserIdentityManager:: disconnessione (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logoff
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 4266e6116e43b7b792c3040d7c86a60037ca4c44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104976991"
---
# <a name="iuseridentitymanagerlogoff-method"></a><span data-ttu-id="7e33d-104">Metodo IUserIdentityManager:: disconnessione</span><span class="sxs-lookup"><span data-stu-id="7e33d-104">IUserIdentityManager::Logoff method</span></span>

<span data-ttu-id="7e33d-105">\[La **disconnessione** non è supportata e può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="7e33d-105">\[**Logoff** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="7e33d-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="7e33d-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="7e33d-107">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7e33d-107">Deprecated.</span></span> <span data-ttu-id="7e33d-108">Disconnettere l'identità corrente.</span><span class="sxs-lookup"><span data-stu-id="7e33d-108">Log off the current identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e33d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e33d-109">Syntax</span></span>


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="7e33d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e33d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e33d-111">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e33d-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e33d-112">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="7e33d-112">Type: **HWND**</span></span>

<span data-ttu-id="7e33d-113">Valore **HWND** che identifica una finestra che verrà portata in primo piano al termine della disconnessione.</span><span class="sxs-lookup"><span data-stu-id="7e33d-113">An **HWND** value that identifies a window that will be brought into the foreground when the logoff is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e33d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e33d-114">Return value</span></span>

<span data-ttu-id="7e33d-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7e33d-115">Type: **HRESULT**</span></span>

<span data-ttu-id="7e33d-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7e33d-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7e33d-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7e33d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e33d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e33d-118">Requirements</span></span>



| <span data-ttu-id="7e33d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e33d-119">Requirement</span></span> | <span data-ttu-id="7e33d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7e33d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e33d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e33d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7e33d-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7e33d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7e33d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e33d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7e33d-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7e33d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7e33d-125">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7e33d-125">End of client support</span></span><br/>    | <span data-ttu-id="7e33d-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7e33d-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="7e33d-127">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="7e33d-127">End of server support</span></span><br/>    | <span data-ttu-id="7e33d-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e33d-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="7e33d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e33d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e33d-130"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e33d-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e33d-131">IDL</span><span class="sxs-lookup"><span data-stu-id="7e33d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7e33d-132"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7e33d-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="7e33d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7e33d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e33d-134"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e33d-134"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e33d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e33d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e33d-136">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="7e33d-136">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="7e33d-137">**IUserIdentityManager:: Logon**</span><span class="sxs-lookup"><span data-stu-id="7e33d-137">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="7e33d-138">**IUserIdentityManager::ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="7e33d-138">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




