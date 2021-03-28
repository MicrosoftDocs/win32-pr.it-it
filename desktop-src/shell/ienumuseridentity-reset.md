---
description: Reimposta il numero interno di interfacce recuperate nell'enumerazione.
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: 'Metodo IEnumUserIdentity:: Reset (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 05b3c5d38575fa1b2957c28070d642ad15f846ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227428"
---
# <a name="ienumuseridentityreset-method"></a><span data-ttu-id="bbc49-103">Metodo IEnumUserIdentity:: Reset</span><span class="sxs-lookup"><span data-stu-id="bbc49-103">IEnumUserIdentity::Reset method</span></span>

<span data-ttu-id="bbc49-104">\[**IEnumUserIdentity:: Reset** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="bbc49-104">\[**IEnumUserIdentity::Reset** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bbc49-105">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="bbc49-105">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="bbc49-106">Reimposta il numero interno di interfacce recuperate nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="bbc49-106">Resets the internal count of retrieved interfaces in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc49-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbc49-107">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="bbc49-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbc49-108">Parameters</span></span>

<span data-ttu-id="bbc49-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bbc49-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbc49-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbc49-110">Return value</span></span>

<span data-ttu-id="bbc49-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bbc49-111">Type: **HRESULT**</span></span>

<span data-ttu-id="bbc49-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bbc49-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bbc49-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bbc49-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbc49-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbc49-114">Remarks</span></span>

<span data-ttu-id="bbc49-115">[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un conteggio interno che specifica l'interfaccia successiva da recuperare.</span><span class="sxs-lookup"><span data-stu-id="bbc49-115">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="bbc49-116">Se si chiama questo metodo, verrà reimpostato il valore di questo conteggio.</span><span class="sxs-lookup"><span data-stu-id="bbc49-116">Calling this method will reset the value of this count.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc49-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbc49-117">Requirements</span></span>



| <span data-ttu-id="bbc49-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbc49-118">Requirement</span></span> | <span data-ttu-id="bbc49-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bbc49-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc49-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbc49-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc49-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bbc49-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bbc49-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbc49-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc49-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bbc49-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bbc49-124">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bbc49-124">End of client support</span></span><br/>    | <span data-ttu-id="bbc49-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bbc49-125">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="bbc49-126">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bbc49-126">End of server support</span></span><br/>    | <span data-ttu-id="bbc49-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bbc49-127">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="bbc49-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbc49-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbc49-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbc49-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbc49-130">IDL</span><span class="sxs-lookup"><span data-stu-id="bbc49-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bbc49-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bbc49-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="bbc49-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bbc49-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbc49-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbc49-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbc49-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbc49-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc49-135">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="bbc49-135">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="bbc49-136">**IEnumUserIdentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="bbc49-136">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="bbc49-137">**IEnumUserIdentity:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="bbc49-137">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> <dt>

[<span data-ttu-id="bbc49-138">**IEnumUserIdentity:: Next**</span><span class="sxs-lookup"><span data-stu-id="bbc49-138">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




