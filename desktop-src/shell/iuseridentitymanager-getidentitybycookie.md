---
description: GetIdentityByCookie non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'Metodo IUserIdentityManager:: GetIdentityByCookie (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb4e5ad5bda349a5b1650b090abc44a9fd1e6332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524441"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a><span data-ttu-id="3b623-104">Metodo IUserIdentityManager:: GetIdentityByCookie</span><span class="sxs-lookup"><span data-stu-id="3b623-104">IUserIdentityManager::GetIdentityByCookie method</span></span>

<span data-ttu-id="3b623-105">\[**GetIdentityByCookie** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="3b623-105">\[**GetIdentityByCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="3b623-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="3b623-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="3b623-107">Ottiene un'identità utente specifica dal cookie usato per identificarla in modo univoco.</span><span class="sxs-lookup"><span data-stu-id="3b623-107">Gets a specific user identity by the cookie used to uniquely identify it.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b623-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b623-108">Syntax</span></span>


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="3b623-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b623-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b623-110">*uidCookie* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b623-110">*uidCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b623-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="3b623-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="3b623-112">Indirizzo di un valore _ *GUID*\* che rappresenta il cookie per l'identità che si vuole recuperare.</span><span class="sxs-lookup"><span data-stu-id="3b623-112">The address of a _ *GUID*\* value that represents the cookie for the identity you want to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="3b623-113">*ppIdentity* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3b623-113">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b623-114">Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3b623-114">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="3b623-115">Indirizzo del puntatore che riceverà l'oggetto identità utente.</span><span class="sxs-lookup"><span data-stu-id="3b623-115">The address of the pointer that will receive the user identity object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b623-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b623-116">Return value</span></span>

<span data-ttu-id="3b623-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3b623-117">Type: **HRESULT**</span></span>

<span data-ttu-id="3b623-118">Risultato della richiesta di recupero.</span><span class="sxs-lookup"><span data-stu-id="3b623-118">The result of the retrieval request.</span></span> <span data-ttu-id="3b623-119">Se ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3b623-119">If successful, it returns S\_OK.</span></span> <span data-ttu-id="3b623-120">In caso contrario, verrà restituito uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="3b623-120">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="3b623-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3b623-121">Return code</span></span>                                                                                            | <span data-ttu-id="3b623-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b623-122">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="3b623-123"><dt>**\_identità E \_ non \_ trovate**</dt></span><span class="sxs-lookup"><span data-stu-id="3b623-123"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="3b623-124">Impossibile trovare l'identità richiesta.</span><span class="sxs-lookup"><span data-stu-id="3b623-124">The identity requested could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="3b623-125"><dt>**\_identità E \_ disabilitate**</dt></span><span class="sxs-lookup"><span data-stu-id="3b623-125"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="3b623-126">Gestione identità è disabilitato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="3b623-126">Identity management is disabled on the system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3b623-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b623-127">Requirements</span></span>



| <span data-ttu-id="3b623-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b623-128">Requirement</span></span> | <span data-ttu-id="3b623-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3b623-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b623-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b623-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3b623-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3b623-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3b623-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b623-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3b623-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3b623-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3b623-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3b623-134">End of client support</span></span><br/>    | <span data-ttu-id="3b623-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3b623-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="3b623-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="3b623-136">End of server support</span></span><br/>    | <span data-ttu-id="3b623-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3b623-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="3b623-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b623-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b623-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b623-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b623-140">IDL</span><span class="sxs-lookup"><span data-stu-id="3b623-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b623-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b623-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="3b623-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3b623-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b623-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b623-143"><dt>Msident.dll</dt></span></span> </dl> |



 

 




