---
description: GetOrdinal non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: 'Metodo IUserIdentity2:: GetOrdinal (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f5a7e875e92342363722858b3ac714171cb547b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980047"
---
# <a name="iuseridentity2getordinal-method"></a><span data-ttu-id="d62eb-104">Metodo IUserIdentity2:: GetOrdinal</span><span class="sxs-lookup"><span data-stu-id="d62eb-104">IUserIdentity2::GetOrdinal method</span></span>

<span data-ttu-id="d62eb-105">\[**GetOrdinal** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="d62eb-105">\[**GetOrdinal** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="d62eb-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="d62eb-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="d62eb-107">Ottiene il numero ordinale per l'identità.</span><span class="sxs-lookup"><span data-stu-id="d62eb-107">Gets the ordinal number for this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="d62eb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d62eb-108">Syntax</span></span>


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a><span data-ttu-id="d62eb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d62eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d62eb-110">*dwOrdinal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d62eb-110">*dwOrdinal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d62eb-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="d62eb-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="d62eb-112">Puntatore a un valore _ *DWORD*\* che riceve il numero ordinale per l'identità.</span><span class="sxs-lookup"><span data-stu-id="d62eb-112">A pointer to a _ *DWORD*\* value that receives the ordinal number for this identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d62eb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d62eb-113">Return value</span></span>

<span data-ttu-id="d62eb-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d62eb-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d62eb-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d62eb-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d62eb-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d62eb-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d62eb-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d62eb-117">Remarks</span></span>

<span data-ttu-id="d62eb-118">Il numero ordinale determina l'ordine delle identità nell'elenco di identità, ma potrebbe non essere mantenuto durante le operazioni sulle identità.</span><span class="sxs-lookup"><span data-stu-id="d62eb-118">The ordinal determines the order of the identities in the identity list, but may not persist throughout operations on the identities.</span></span> <span data-ttu-id="d62eb-119">Per ottenere un valore univoco per un'identità, chiamare [**GetCookie**](iuseridentity-getcookie.md).</span><span class="sxs-lookup"><span data-stu-id="d62eb-119">To get a unique value for an identity, call [**GetCookie**](iuseridentity-getcookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d62eb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d62eb-120">Requirements</span></span>



| <span data-ttu-id="d62eb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d62eb-121">Requirement</span></span> | <span data-ttu-id="d62eb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d62eb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d62eb-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d62eb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d62eb-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d62eb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d62eb-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d62eb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d62eb-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d62eb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d62eb-127">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d62eb-127">End of client support</span></span><br/>    | <span data-ttu-id="d62eb-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d62eb-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="d62eb-129">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="d62eb-129">End of server support</span></span><br/>    | <span data-ttu-id="d62eb-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d62eb-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="d62eb-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d62eb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d62eb-132"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="d62eb-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="d62eb-133">IDL</span><span class="sxs-lookup"><span data-stu-id="d62eb-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d62eb-134"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d62eb-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="d62eb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d62eb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d62eb-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d62eb-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d62eb-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d62eb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d62eb-138">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="d62eb-138">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="d62eb-139">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="d62eb-139">**GetCookie**</span></span>](iuseridentity-getcookie.md)
</dt> </dl>

 

 




