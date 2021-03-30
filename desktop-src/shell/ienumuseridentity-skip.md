---
description: 'IEnumUserIdentity:: Skip non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.'
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: 'Metodo IEnumUserIdentity:: Skip (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: cedd4f3c6e9736e26cbf8d58f27f805f0f5d33a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994600"
---
# <a name="ienumuseridentityskip-method"></a><span data-ttu-id="6491b-104">Metodo IEnumUserIdentity:: Skip</span><span class="sxs-lookup"><span data-stu-id="6491b-104">IEnumUserIdentity::Skip method</span></span>

<span data-ttu-id="6491b-105">\[**IEnumUserIdentity:: Skip** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="6491b-105">\[**IEnumUserIdentity::Skip** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="6491b-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="6491b-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="6491b-107">Ignora un determinato numero di interfacce di identità utente nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="6491b-107">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="6491b-108">Utilizzato durante il recupero delle interfacce.</span><span class="sxs-lookup"><span data-stu-id="6491b-108">Used when retrieving interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="6491b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6491b-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="6491b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6491b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6491b-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6491b-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6491b-112">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="6491b-112">Type: **ULONG**</span></span>

<span data-ttu-id="6491b-113">Numero di interfacce da ignorare.</span><span class="sxs-lookup"><span data-stu-id="6491b-113">The number of interfaces to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6491b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6491b-114">Return value</span></span>

<span data-ttu-id="6491b-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6491b-115">Type: **HRESULT**</span></span>

<span data-ttu-id="6491b-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6491b-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6491b-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6491b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6491b-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="6491b-118">Remarks</span></span>

<span data-ttu-id="6491b-119">[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un conteggio interno che specifica l'interfaccia successiva da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6491b-119">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="6491b-120">Per incrementare il conteggio senza recuperare le interfacce, chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="6491b-120">To increment this count without retrieving interfaces, call this method.</span></span> <span data-ttu-id="6491b-121">Per reimpostare il conteggio, chiamare [**IEnumUserIdentity:: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="6491b-121">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6491b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6491b-122">Requirements</span></span>



| <span data-ttu-id="6491b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6491b-123">Requirement</span></span> | <span data-ttu-id="6491b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6491b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6491b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6491b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6491b-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6491b-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6491b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6491b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6491b-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6491b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6491b-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6491b-129">End of client support</span></span><br/>    | <span data-ttu-id="6491b-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6491b-130">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="6491b-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6491b-131">End of server support</span></span><br/>    | <span data-ttu-id="6491b-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6491b-132">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="6491b-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6491b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6491b-134"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="6491b-134"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="6491b-135">IDL</span><span class="sxs-lookup"><span data-stu-id="6491b-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6491b-136"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6491b-136"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="6491b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6491b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6491b-138"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6491b-138"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6491b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6491b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6491b-140">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="6491b-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="6491b-141">**IEnumUserIdentity:: Reset**</span><span class="sxs-lookup"><span data-stu-id="6491b-141">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="6491b-142">**IEnumUserIdentity:: Next**</span><span class="sxs-lookup"><span data-stu-id="6491b-142">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> <dt>

[<span data-ttu-id="6491b-143">**IEnumUserIdentity:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="6491b-143">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 




