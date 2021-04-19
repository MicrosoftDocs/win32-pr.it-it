---
title: Funzione MpThreatQuery (MpClient. h)
description: Utilizzato per eseguire una query su una particolare minaccia, ad esempio la gravità e la categoria, o localizzata, ad esempio una descrizione della categoria e consigli.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpThreatQuery
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301404"
---
# <a name="mpthreatquery-function"></a><span data-ttu-id="57e87-104">MpThreatQuery (funzione)</span><span class="sxs-lookup"><span data-stu-id="57e87-104">MpThreatQuery function</span></span>

<span data-ttu-id="57e87-105">Utilizzato per eseguire una query su una particolare minaccia, ad esempio la gravità e la categoria, o localizzata, ad esempio una descrizione della categoria e consigli.</span><span class="sxs-lookup"><span data-stu-id="57e87-105">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="57e87-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57e87-106">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a><span data-ttu-id="57e87-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="57e87-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57e87-108">*hMpHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57e87-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57e87-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="57e87-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="57e87-110">Handle per l'interfaccia di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="57e87-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="57e87-111">Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="57e87-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="57e87-112">*ThreatID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57e87-112">*ThreatID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57e87-113">Tipo: **MPTHREAT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="57e87-113">Type: **MPTHREAT\_ID**</span></span>

<span data-ttu-id="57e87-114">Identificatore di minaccia per il quale vengono richieste informazioni.</span><span class="sxs-lookup"><span data-stu-id="57e87-114">Threat identifier for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="57e87-115">*ppThreatInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57e87-115">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57e87-116">Tipo: \**PMPTHREAT \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="57e87-116">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="57e87-117">Restituisce un puntatore a una struttura di informazioni sulle minacce, [_ *MPTHREAT \_ info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="57e87-117">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="57e87-118">La struttura contiene informazioni quali ID minaccia, nome e gravità.</span><span class="sxs-lookup"><span data-stu-id="57e87-118">The structure contains information such as threat id, name, and severity.</span></span>

</dd> <dt>

<span data-ttu-id="57e87-119">*ppThreatLocalizedInfo* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="57e87-119">*ppThreatLocalizedInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="57e87-120">Tipo: \**PMPTHREAT \_ \_ informazioni \* localizzate* _</span><span class="sxs-lookup"><span data-stu-id="57e87-120">Type: \**PMPTHREAT\_LOCALIZED\_INFO\** _</span></span>

<span data-ttu-id="57e87-121">Restituisce un puntatore a una struttura contenente le informazioni localizzate sulla minaccia.</span><span class="sxs-lookup"><span data-stu-id="57e87-121">Returns a pointer to a structure containing localized information about the threat.</span></span> <span data-ttu-id="57e87-122">È possibile passare _ *null*\* se non si è interessati alle informazioni localizzate sulla minaccia.</span><span class="sxs-lookup"><span data-stu-id="57e87-122">You can pass _ *NULL*\* if you are not interested in localized information about the threat.</span></span> <span data-ttu-id="57e87-123">Vedere [**le \_ \_ informazioni localizzate MPTHREAT**](mpthreat-localized-info.md).</span><span class="sxs-lookup"><span data-stu-id="57e87-123">See [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57e87-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57e87-124">Return value</span></span>

<span data-ttu-id="57e87-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="57e87-125">Type: **HRESULT**</span></span>

<span data-ttu-id="57e87-126">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="57e87-126">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="57e87-127">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="57e87-127">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="57e87-128">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="57e87-128">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="57e87-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57e87-129">Requirements</span></span>



| <span data-ttu-id="57e87-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="57e87-130">Requirement</span></span> | <span data-ttu-id="57e87-131">Valore</span><span class="sxs-lookup"><span data-stu-id="57e87-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57e87-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57e87-132">Minimum supported client</span></span><br/> | <span data-ttu-id="57e87-133">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="57e87-133">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="57e87-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57e87-134">Minimum supported server</span></span><br/> | <span data-ttu-id="57e87-135">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="57e87-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57e87-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57e87-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="57e87-137"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="57e87-137"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="57e87-138">DLL</span><span class="sxs-lookup"><span data-stu-id="57e87-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57e87-139"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57e87-139"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57e87-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57e87-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57e87-141">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="57e87-141">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="57e87-142">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="57e87-142">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="57e87-143">**\_informazioni MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="57e87-143">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="57e87-144">**\_informazioni localizzate MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="57e87-144">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





