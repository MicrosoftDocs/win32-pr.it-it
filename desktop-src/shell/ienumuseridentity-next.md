---
description: 'IEnumUserIdentity:: Next non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'Metodo IEnumUserIdentity:: Next (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 763b2b4a612596c5f02a9826ad2e9c09ab8e4b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994608"
---
# <a name="ienumuseridentitynext-method"></a><span data-ttu-id="013bd-104">IEnumUserIdentity:: Next (metodo)</span><span class="sxs-lookup"><span data-stu-id="013bd-104">IEnumUserIdentity::Next method</span></span>

<span data-ttu-id="013bd-105">\[**IEnumUserIdentity:: Next** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="013bd-105">\[**IEnumUserIdentity::Next** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="013bd-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="013bd-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="013bd-107">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="013bd-107">Deprecated.</span></span> <span data-ttu-id="013bd-108">Recupera una matrice di interfacce di identità utente dall'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="013bd-108">Retrieves an array of user identity interfaces from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="013bd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="013bd-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="013bd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="013bd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="013bd-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="013bd-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="013bd-112">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="013bd-112">Type: **ULONG**</span></span>

<span data-ttu-id="013bd-113">Valore **ULONG** che rappresenta il numero di interfacce da recuperare.</span><span class="sxs-lookup"><span data-stu-id="013bd-113">A **ULONG** value that represents the number of interfaces to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="013bd-114">*rgelt* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="013bd-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="013bd-115">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="013bd-115">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="013bd-116">Indirizzo di un puntatore che riceve le interfacce.</span><span class="sxs-lookup"><span data-stu-id="013bd-116">The address of a pointer that receives the interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="013bd-117">*pceltFetched* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="013bd-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="013bd-118">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="013bd-118">Type: \**ULONG\** _</span></span>

<span data-ttu-id="013bd-119">Indirizzo di un puntatore che riceve il numero di interfacce recuperate correttamente.</span><span class="sxs-lookup"><span data-stu-id="013bd-119">The address of a pointer that receives the number of interfaces successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="013bd-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="013bd-120">Return value</span></span>

<span data-ttu-id="013bd-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="013bd-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="013bd-122">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="013bd-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="013bd-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="013bd-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="013bd-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="013bd-124">Remarks</span></span>

<span data-ttu-id="013bd-125">[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un conteggio interno che specifica l'interfaccia successiva da recuperare.</span><span class="sxs-lookup"><span data-stu-id="013bd-125">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="013bd-126">Per più chiamate a questo metodo non verrà reimpostato questo conteggio.</span><span class="sxs-lookup"><span data-stu-id="013bd-126">Multiple calls to this method will not reset this count.</span></span> <span data-ttu-id="013bd-127">Per reimpostare il conteggio, chiamare [**IEnumUserIdentity:: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="013bd-127">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span> <span data-ttu-id="013bd-128">Per incrementare il conteggio senza recuperare le interfacce, chiamare [**IEnumUserIdentity:: Skip**](ienumuseridentity-skip.md).</span><span class="sxs-lookup"><span data-stu-id="013bd-128">To increment the count without retrieving interfaces, call [**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md).</span></span>

<span data-ttu-id="013bd-129">Il valore di *celt* non deve superare il valore restituito da [**IEnumUserIdentity:: GetCount**](ienumuseridentity-getcount.md).</span><span class="sxs-lookup"><span data-stu-id="013bd-129">The value of *celt* should not exceed the value returned by [**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="013bd-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="013bd-130">Requirements</span></span>



| <span data-ttu-id="013bd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="013bd-131">Requirement</span></span> | <span data-ttu-id="013bd-132">Valore</span><span class="sxs-lookup"><span data-stu-id="013bd-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="013bd-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="013bd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="013bd-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="013bd-134">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="013bd-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="013bd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="013bd-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="013bd-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="013bd-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="013bd-137">End of client support</span></span><br/>    | <span data-ttu-id="013bd-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="013bd-138">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="013bd-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="013bd-139">End of server support</span></span><br/>    | <span data-ttu-id="013bd-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="013bd-140">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="013bd-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="013bd-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="013bd-142"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="013bd-142"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="013bd-143">IDL</span><span class="sxs-lookup"><span data-stu-id="013bd-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="013bd-144"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="013bd-144"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="013bd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="013bd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="013bd-146"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="013bd-146"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="013bd-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="013bd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="013bd-148">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="013bd-148">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="013bd-149">**IEnumUserIdentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="013bd-149">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="013bd-150">**IEnumUserIdentity:: Reset**</span><span class="sxs-lookup"><span data-stu-id="013bd-150">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="013bd-151">**IEnumUserIdentity:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="013bd-151">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
