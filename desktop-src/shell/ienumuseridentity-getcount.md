---
description: GetCount non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: 'Metodo IEnumUserIdentity:: GetCount (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 43355a9585fc4099c8649f7df506ff3495a53944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345386"
---
# <a name="ienumuseridentitygetcount-method"></a><span data-ttu-id="57b60-104">Metodo IEnumUserIdentity:: GetCount</span><span class="sxs-lookup"><span data-stu-id="57b60-104">IEnumUserIdentity::GetCount method</span></span>

<span data-ttu-id="57b60-105">\[**GetCount** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="57b60-105">\[**GetCount** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="57b60-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="57b60-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="57b60-107">Ottiene il numero di identità utente attualmente presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="57b60-107">Gets the count of user identities currently on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="57b60-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57b60-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a><span data-ttu-id="57b60-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="57b60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b60-110">*pnCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57b60-110">*pnCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57b60-111">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="57b60-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="57b60-112">Puntatore a un _ *ULONG*\* che riceve il conteggio.</span><span class="sxs-lookup"><span data-stu-id="57b60-112">Pointer to a _ *ULONG*\* that receives the count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b60-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57b60-113">Return value</span></span>

<span data-ttu-id="57b60-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="57b60-114">Type: **HRESULT**</span></span>

<span data-ttu-id="57b60-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="57b60-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57b60-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57b60-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57b60-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="57b60-117">Remarks</span></span>

<span data-ttu-id="57b60-118">Se il supporto per più identità utente è disabilitato, *pnCount* riceverà il valore 1.</span><span class="sxs-lookup"><span data-stu-id="57b60-118">If support for multiple user identities is disabled, *pnCount* will receive a value of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="57b60-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57b60-119">Requirements</span></span>



| <span data-ttu-id="57b60-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="57b60-120">Requirement</span></span> | <span data-ttu-id="57b60-121">Valore</span><span class="sxs-lookup"><span data-stu-id="57b60-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57b60-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57b60-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57b60-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="57b60-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="57b60-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57b60-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57b60-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="57b60-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="57b60-126">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="57b60-126">End of client support</span></span><br/>    | <span data-ttu-id="57b60-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="57b60-127">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="57b60-128">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="57b60-128">End of server support</span></span><br/>    | <span data-ttu-id="57b60-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="57b60-129">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="57b60-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57b60-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="57b60-131"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="57b60-131"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="57b60-132">IDL</span><span class="sxs-lookup"><span data-stu-id="57b60-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57b60-133"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="57b60-133"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="57b60-134">DLL</span><span class="sxs-lookup"><span data-stu-id="57b60-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57b60-135"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57b60-135"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57b60-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57b60-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b60-137">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="57b60-137">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="57b60-138">**IEnumUserIdentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="57b60-138">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="57b60-139">**IEnumUserIdentity:: Reset**</span><span class="sxs-lookup"><span data-stu-id="57b60-139">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="57b60-140">**IEnumUserIdentity:: Next**</span><span class="sxs-lookup"><span data-stu-id="57b60-140">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




