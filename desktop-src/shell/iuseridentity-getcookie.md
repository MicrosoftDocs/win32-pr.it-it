---
description: GetCookie non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 4a743d64-9af3-43cf-9a9f-d808676ab337
title: 'Metodo IUserIdentity:: GetCookie (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 96cafb13f2c90c41e4aa6dcaaa72cf052757d0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977914"
---
# <a name="iuseridentitygetcookie-method"></a><span data-ttu-id="a06d1-104">Metodo IUserIdentity:: GetCookie</span><span class="sxs-lookup"><span data-stu-id="a06d1-104">IUserIdentity::GetCookie method</span></span>

<span data-ttu-id="a06d1-105">\[**GetCookie** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="a06d1-105">\[**GetCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="a06d1-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="a06d1-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="a06d1-107">Ottiene il cookie utilizzato per identificare in modo univoco l'identità dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a06d1-107">Gets the cookie used to uniquely identify this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="a06d1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a06d1-108">Syntax</span></span>


```C++
HRESULT GetCookie(
  [out] GUID *puidCookie
);
```



## <a name="parameters"></a><span data-ttu-id="a06d1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a06d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a06d1-110">*puidCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a06d1-110">*puidCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a06d1-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="a06d1-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="a06d1-112">Puntatore a un valore _ *GUID*\* che riceve il cookie usato per identificare in modo univoco questa identità utente.</span><span class="sxs-lookup"><span data-stu-id="a06d1-112">A pointer to a _ *GUID*\* value that receives the cookie used to uniquely identify this user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a06d1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a06d1-113">Return value</span></span>

<span data-ttu-id="a06d1-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a06d1-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a06d1-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a06d1-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a06d1-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a06d1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a06d1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a06d1-117">Requirements</span></span>



| <span data-ttu-id="a06d1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a06d1-118">Requirement</span></span> | <span data-ttu-id="a06d1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a06d1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a06d1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a06d1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a06d1-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a06d1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a06d1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a06d1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a06d1-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a06d1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a06d1-124">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a06d1-124">End of client support</span></span><br/>    | <span data-ttu-id="a06d1-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a06d1-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a06d1-126">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a06d1-126">End of server support</span></span><br/>    | <span data-ttu-id="a06d1-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a06d1-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a06d1-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a06d1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a06d1-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="a06d1-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="a06d1-130">IDL</span><span class="sxs-lookup"><span data-stu-id="a06d1-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a06d1-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a06d1-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="a06d1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a06d1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a06d1-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a06d1-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a06d1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a06d1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a06d1-135">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="a06d1-135">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="a06d1-136">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="a06d1-136">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)
</dt> </dl>

 

 




