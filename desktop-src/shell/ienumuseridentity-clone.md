---
description: 'IEnumUserIdentity:: clone non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: 'Metodo IEnumUserIdentity:: Clone (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: ebdec426fe7ab591c801c00b637211e903cf5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994613"
---
# <a name="ienumuseridentityclone-method"></a><span data-ttu-id="2e475-104">Metodo IEnumUserIdentity:: Clone</span><span class="sxs-lookup"><span data-stu-id="2e475-104">IEnumUserIdentity::Clone method</span></span>

<span data-ttu-id="2e475-105">\[**IEnumUserIdentity:: Clone** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="2e475-105">\[**IEnumUserIdentity::Clone** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="2e475-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="2e475-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="2e475-107">Ottiene una copia dell'enumerazione corrente.</span><span class="sxs-lookup"><span data-stu-id="2e475-107">Gets a copy of the current enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e475-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e475-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="2e475-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e475-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e475-110">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2e475-110">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e475-111">Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2e475-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="2e475-112">Indirizzo di un puntatore che riceve una copia di questa enumerazione.</span><span class="sxs-lookup"><span data-stu-id="2e475-112">The address of a pointer that receives a copy of this enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e475-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e475-113">Return value</span></span>

<span data-ttu-id="2e475-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2e475-114">Type: **HRESULT**</span></span>

<span data-ttu-id="2e475-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2e475-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e475-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e475-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e475-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e475-117">Remarks</span></span>

<span data-ttu-id="2e475-118">[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un conteggio interno che specifica l'interfaccia successiva da recuperare.</span><span class="sxs-lookup"><span data-stu-id="2e475-118">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="2e475-119">Il valore di questo conteggio verrà applicato all'interfaccia ricevuta da *ppEnum*.</span><span class="sxs-lookup"><span data-stu-id="2e475-119">The value of this count will be applied to the interface received by *ppenum*.</span></span> <span data-ttu-id="2e475-120">Per reimpostare il conteggio, chiamare [**IEnumUserIdentity:: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="2e475-120">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e475-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e475-121">Requirements</span></span>



| <span data-ttu-id="2e475-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e475-122">Requirement</span></span> | <span data-ttu-id="2e475-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2e475-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e475-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e475-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2e475-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2e475-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2e475-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e475-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2e475-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e475-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2e475-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2e475-128">End of client support</span></span><br/>    | <span data-ttu-id="2e475-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2e475-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="2e475-130">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2e475-130">End of server support</span></span><br/>    | <span data-ttu-id="2e475-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e475-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="2e475-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e475-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e475-133"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e475-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e475-134">IDL</span><span class="sxs-lookup"><span data-stu-id="2e475-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e475-135"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e475-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="2e475-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2e475-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e475-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e475-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e475-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e475-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e475-139">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="2e475-139">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="2e475-140">**IEnumUserIdentity:: Reset**</span><span class="sxs-lookup"><span data-stu-id="2e475-140">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> </dl>

 

 




