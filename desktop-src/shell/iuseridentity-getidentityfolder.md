---
description: GetIdentityFolder non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: 'Metodo IUserIdentity:: GetIdentityFolder (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 9f2644570bb7ccc2ae5bee8a37d4471ffb65861a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977903"
---
# <a name="iuseridentitygetidentityfolder-method"></a><span data-ttu-id="6104f-104">Metodo IUserIdentity:: GetIdentityFolder</span><span class="sxs-lookup"><span data-stu-id="6104f-104">IUserIdentity::GetIdentityFolder method</span></span>

<span data-ttu-id="6104f-105">\[**GetIdentityFolder** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="6104f-105">\[**GetIdentityFolder** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="6104f-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="6104f-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="6104f-107">Ottiene la cartella di file associata a questa identità.</span><span class="sxs-lookup"><span data-stu-id="6104f-107">Gets the file folder associated with this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="6104f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6104f-108">Syntax</span></span>


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="6104f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6104f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6104f-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6104f-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6104f-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6104f-111">Type: **DWORD**</span></span>

<span data-ttu-id="6104f-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6104f-112">Required.</span></span> <span data-ttu-id="6104f-113">Valore che specifica se la cartella associata a questa identità è in roaming.</span><span class="sxs-lookup"><span data-stu-id="6104f-113">A value that specifies whether the folder associated with this identity is roaming.</span></span> <span data-ttu-id="6104f-114">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6104f-114">Must be one of the following values.</span></span>

<dt>



 <span data-ttu-id="6104f-115">(GIF \_ cartella ROAMing \_ )</span><span class="sxs-lookup"><span data-stu-id="6104f-115">(GIF\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="6104f-116">La cartella è in roaming.</span><span class="sxs-lookup"><span data-stu-id="6104f-116">The folder is roaming.</span></span>

</dd> <dt>



 <span data-ttu-id="6104f-117">(GIF \_ cartella NON in \_ roaming \_ )</span><span class="sxs-lookup"><span data-stu-id="6104f-117">(GIF\_NON\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="6104f-118">La cartella è locale.</span><span class="sxs-lookup"><span data-stu-id="6104f-118">The folder is local.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6104f-119">*pszPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6104f-119">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6104f-120">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="6104f-120">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="6104f-121">Puntatore a una stringa di caratteri wide che riceve il percorso della cartella.</span><span class="sxs-lookup"><span data-stu-id="6104f-121">A pointer to a wide-character string that receives the folder path.</span></span>

</dd> <dt>

<span data-ttu-id="6104f-122">_ulBuffSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6104f-122">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6104f-123">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="6104f-123">Type: **ULONG**</span></span>

<span data-ttu-id="6104f-124">Valore che specifica la dimensione di *pszPath*.</span><span class="sxs-lookup"><span data-stu-id="6104f-124">A value that specifies the size of *pszPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6104f-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6104f-125">Return value</span></span>

<span data-ttu-id="6104f-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6104f-126">Type: **HRESULT**</span></span>

<span data-ttu-id="6104f-127">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6104f-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6104f-128">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6104f-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6104f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6104f-129">Requirements</span></span>



| <span data-ttu-id="6104f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6104f-130">Requirement</span></span> | <span data-ttu-id="6104f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="6104f-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6104f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6104f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6104f-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6104f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6104f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6104f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6104f-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6104f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6104f-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6104f-136">End of client support</span></span><br/>    | <span data-ttu-id="6104f-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6104f-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="6104f-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6104f-138">End of server support</span></span><br/>    | <span data-ttu-id="6104f-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6104f-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="6104f-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6104f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6104f-141"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="6104f-141"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="6104f-142">IDL</span><span class="sxs-lookup"><span data-stu-id="6104f-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6104f-143"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6104f-143"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="6104f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6104f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6104f-145"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6104f-145"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6104f-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6104f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6104f-147">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="6104f-147">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="6104f-148">**IUserIdentity::OpenIdentityRegKey**</span><span class="sxs-lookup"><span data-stu-id="6104f-148">**IUserIdentity::OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




