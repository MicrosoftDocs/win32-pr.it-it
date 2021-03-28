---
description: 'IUserIdentityManager:: EnumIdentities non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'Metodo IUserIdentityManager:: EnumIdentities (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127834"
---
# <a name="iuseridentitymanagerenumidentities-method"></a><span data-ttu-id="5c457-104">Metodo IUserIdentityManager:: EnumIdentities</span><span class="sxs-lookup"><span data-stu-id="5c457-104">IUserIdentityManager::EnumIdentities method</span></span>

<span data-ttu-id="5c457-105">\[**IUserIdentityManager:: EnumIdentities** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="5c457-105">\[**IUserIdentityManager::EnumIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="5c457-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="5c457-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="5c457-107">Ottiene un oggetto [**IEnumUserIdentity**](ienumuseridentity.md) che può essere utilizzato per enumerare le identità utente presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5c457-107">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c457-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c457-108">Syntax</span></span>


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a><span data-ttu-id="5c457-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c457-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c457-110">*ppEnumUser* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c457-110">*ppEnumUser* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c457-111">Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5c457-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="5c457-112">Indirizzo del puntatore al nuovo oggetto di enumerazione di identità.</span><span class="sxs-lookup"><span data-stu-id="5c457-112">The address of the pointer to the new identity enumeration object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c457-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c457-113">Return value</span></span>

<span data-ttu-id="5c457-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5c457-114">Type: **HRESULT**</span></span>

<span data-ttu-id="5c457-115">Risultato dell'operazione di recupero.</span><span class="sxs-lookup"><span data-stu-id="5c457-115">The result of the retrieval operation.</span></span> <span data-ttu-id="5c457-116">Se ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5c457-116">If successful, it returns S\_OK.</span></span> <span data-ttu-id="5c457-117">Se non è stato possibile creare l'oggetto di enumerazione, viene restituito E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="5c457-117">If the enumeration object could not be created, it returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c457-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c457-118">Remarks</span></span>

<span data-ttu-id="5c457-119">Questo metodo è utile per l'iterazione dell'elenco di identità nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5c457-119">This method is useful for iteration over the list of identities on the system.</span></span> <span data-ttu-id="5c457-120">Per recuperare una singola identità tramite il cookie senza accedere all'elenco, chiamare [**IUserIdentityManager:: GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).</span><span class="sxs-lookup"><span data-stu-id="5c457-120">To retrieve a single identity by its cookie without accessing the list, call [**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c457-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c457-121">Requirements</span></span>



| <span data-ttu-id="5c457-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c457-122">Requirement</span></span> | <span data-ttu-id="5c457-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5c457-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c457-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c457-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5c457-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c457-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5c457-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c457-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5c457-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c457-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5c457-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5c457-128">End of client support</span></span><br/>    | <span data-ttu-id="5c457-129">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5c457-129">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="5c457-130">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="5c457-130">End of server support</span></span><br/>    | <span data-ttu-id="5c457-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5c457-131">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="5c457-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c457-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c457-133"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c457-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c457-134">IDL</span><span class="sxs-lookup"><span data-stu-id="5c457-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c457-135"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c457-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="5c457-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5c457-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c457-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c457-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c457-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c457-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c457-139">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="5c457-139">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="5c457-140">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="5c457-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="5c457-141">**IUserIdentityManager::GetIdentityByCookie**</span><span class="sxs-lookup"><span data-stu-id="5c457-141">**IUserIdentityManager::GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




