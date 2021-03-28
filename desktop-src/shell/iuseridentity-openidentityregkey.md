---
description: Deprecato. Recupera la chiave nel registro di sistema che corrisponde a questa identità utente.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'Metodo IUserIdentity:: OpenIdentityRegKey (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977895"
---
# <a name="iuseridentityopenidentityregkey-method"></a><span data-ttu-id="e8ee7-104">Metodo IUserIdentity:: OpenIdentityRegKey</span><span class="sxs-lookup"><span data-stu-id="e8ee7-104">IUserIdentity::OpenIdentityRegKey method</span></span>

<span data-ttu-id="e8ee7-105">\[Il metodo **IUserIdentity:: OpenIdentityRegKey** è disponibile per l'uso in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e8ee7-105">\[The **IUserIdentity::OpenIdentityRegKey** method is available for use in Windows 2000.</span></span> <span data-ttu-id="e8ee7-106">In Windows XP questa funzionalità è stata sostituita dagli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md)e potrebbe essere modificata o non disponibile nelle versioni successive.\]</span><span class="sxs-lookup"><span data-stu-id="e8ee7-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="e8ee7-107">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e8ee7-107">Deprecated.</span></span> <span data-ttu-id="e8ee7-108">Recupera la chiave nel registro di sistema che corrisponde a questa identità utente.</span><span class="sxs-lookup"><span data-stu-id="e8ee7-108">Retrieves the key in the registry that corresponds to this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ee7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8ee7-109">Syntax</span></span>


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a><span data-ttu-id="e8ee7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8ee7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8ee7-111">*dwDesiredAccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8ee7-111">*dwDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ee7-112">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e8ee7-112">Type: **DWORD**</span></span>

<span data-ttu-id="e8ee7-113">Valore che descrive il livello di accesso richiesto dalla chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e8ee7-113">A value that describes the access level requested of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="e8ee7-114">*phKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e8ee7-114">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ee7-115">Tipo: \**HKEY \** _</span><span class="sxs-lookup"><span data-stu-id="e8ee7-115">Type: \**HKEY\** _</span></span>

<span data-ttu-id="e8ee7-116">Puntatore che riceve la chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e8ee7-116">A pointer that receives the registry key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8ee7-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8ee7-117">Return value</span></span>

<span data-ttu-id="e8ee7-118">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e8ee7-118">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e8ee7-119">Risultato della richiesta del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e8ee7-119">The result of the registry request.</span></span> <span data-ttu-id="e8ee7-120">Se ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e8ee7-120">If successful, it returns **S\_OK**.</span></span> <span data-ttu-id="e8ee7-121">In caso contrario, verrà restituito uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8ee7-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="e8ee7-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e8ee7-122">Return code</span></span>                                                                                            | <span data-ttu-id="e8ee7-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8ee7-123">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8ee7-124"><dt>**\_identità E \_ non \_ trovate**</dt></span><span class="sxs-lookup"><span data-stu-id="e8ee7-124"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="e8ee7-125">A questa identità non è associata una chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e8ee7-125">This identity does not have an associated registry key.</span></span><br/> |
| <dl> <span data-ttu-id="e8ee7-126"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="e8ee7-126"><dt>**E\_FAIL**</dt></span></span> </dl>                 | <span data-ttu-id="e8ee7-127">Impossibile accedere alla chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e8ee7-127">The registry key was unable to be accessed.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="e8ee7-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8ee7-128">Remarks</span></span>

<span data-ttu-id="e8ee7-129">Il parametro *dwDesiredAccess* è un descrittore di sicurezza di accesso al registro di sistema standard che descrive l'accesso che si desidera ottenere alla chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e8ee7-129">The *dwDesiredAccess* parameter is a standard registry access security descriptor that describes the access you want to gain to the registry key.</span></span> <span data-ttu-id="e8ee7-130">Per altre informazioni sulla sicurezza del registro di sistema, incluso un elenco di valori accettabili per questo parametro, vedere [sicurezza e diritti di accesso per la chiave del registro di sistema](../sysinfo/registry-key-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="e8ee7-130">For more information on registry security, including a list of acceptable values for this parameter, see [Registry Key Security and Access Rights](../sysinfo/registry-key-security-and-access-rights.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8ee7-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8ee7-131">Requirements</span></span>



| <span data-ttu-id="e8ee7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8ee7-132">Requirement</span></span> | <span data-ttu-id="e8ee7-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e8ee7-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ee7-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8ee7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e8ee7-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8ee7-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e8ee7-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8ee7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e8ee7-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8ee7-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e8ee7-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8ee7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8ee7-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8ee7-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8ee7-140">IDL</span><span class="sxs-lookup"><span data-stu-id="e8ee7-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e8ee7-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e8ee7-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="e8ee7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e8ee7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8ee7-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8ee7-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8ee7-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8ee7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8ee7-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="e8ee7-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="e8ee7-146">**IUserIdentity::GetIdentityFolder**</span><span class="sxs-lookup"><span data-stu-id="e8ee7-146">**IUserIdentity::GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
