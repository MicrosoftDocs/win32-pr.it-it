---
title: Funzione MpThreatEnumerate (MpClient. h)
description: Restituisce informazioni sulla minaccia successiva nell'elenco di enumerazione. Questa funzione può essere chiamata ripetutamente fino al completamento dell'enumerazione di tutte le minacce.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpThreatEnumerate
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964587"
---
# <a name="mpthreatenumerate-function"></a><span data-ttu-id="acf09-105">MpThreatEnumerate (funzione)</span><span class="sxs-lookup"><span data-stu-id="acf09-105">MpThreatEnumerate function</span></span>

<span data-ttu-id="acf09-106">Restituisce informazioni sulla minaccia successiva nell'elenco di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="acf09-106">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="acf09-107">Questa funzione può essere chiamata ripetutamente fino al completamento dell'enumerazione di tutte le minacce.</span><span class="sxs-lookup"><span data-stu-id="acf09-107">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf09-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="acf09-108">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a><span data-ttu-id="acf09-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="acf09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf09-110">*hThreatEnumHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="acf09-110">*hThreatEnumHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acf09-111">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="acf09-111">Type: **MPHANDLE**</span></span>

<span data-ttu-id="acf09-112">Handle per un contesto di enumerazione delle minacce restituito da [**MpThreatOpen**](mpthreatopen.md).</span><span class="sxs-lookup"><span data-stu-id="acf09-112">Handle to a threat enumeration context returned by [**MpThreatOpen**](mpthreatopen.md).</span></span>

</dd> <dt>

<span data-ttu-id="acf09-113">*ppThreatInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="acf09-113">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acf09-114">Tipo: \**PMPTHREAT \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="acf09-114">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="acf09-115">Restituisce un puntatore a una struttura di informazioni sulle minacce, [_ *MPTHREAT \_ info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="acf09-115">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="acf09-116">La struttura contiene informazioni quali ID minaccia, nome e gravità.</span><span class="sxs-lookup"><span data-stu-id="acf09-116">The structure contains information such as threat id, name, and severity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf09-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="acf09-117">Return value</span></span>

<span data-ttu-id="acf09-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="acf09-118">Type: **HRESULT**</span></span>

<span data-ttu-id="acf09-119">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="acf09-119">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="acf09-120">Se non sono presenti altri elementi da restituire, il valore restituito è **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="acf09-120">If there are no more items to return the return value is **S\_FALSE**.</span></span>

<span data-ttu-id="acf09-121">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="acf09-121">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="acf09-122">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="acf09-122">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="acf09-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acf09-123">Requirements</span></span>



| <span data-ttu-id="acf09-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="acf09-124">Requirement</span></span> | <span data-ttu-id="acf09-125">Valore</span><span class="sxs-lookup"><span data-stu-id="acf09-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acf09-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acf09-126">Minimum supported client</span></span><br/> | <span data-ttu-id="acf09-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="acf09-127">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="acf09-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acf09-128">Minimum supported server</span></span><br/> | <span data-ttu-id="acf09-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="acf09-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="acf09-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="acf09-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="acf09-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="acf09-131"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="acf09-132">DLL</span><span class="sxs-lookup"><span data-stu-id="acf09-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acf09-133"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acf09-133"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acf09-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="acf09-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf09-135">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="acf09-135">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="acf09-136">**MpThreatOpen**</span><span class="sxs-lookup"><span data-stu-id="acf09-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> <dt>

[<span data-ttu-id="acf09-137">**\_informazioni MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="acf09-137">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> </dl>

 

 





