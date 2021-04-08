---
description: Il metodo KsQueryMediums recupera i supporti supportati da un PIN.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'Metodo IKsPin:: KsQueryMediums (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746575"
---
# <a name="ikspinksquerymediums-method"></a><span data-ttu-id="1f9d0-103">Metodo IKsPin:: KsQueryMediums</span><span class="sxs-lookup"><span data-stu-id="1f9d0-103">IKsPin::KsQueryMediums method</span></span>

<span data-ttu-id="1f9d0-104">Il `KsQueryMediums` metodo recupera i supporti supportati da un PIN.</span><span class="sxs-lookup"><span data-stu-id="1f9d0-104">The `KsQueryMediums` method retrieves the mediums supported by a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f9d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f9d0-105">Syntax</span></span>


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a><span data-ttu-id="1f9d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f9d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f9d0-107">*PPMI* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1f9d0-107">*ppmi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f9d0-108">Indirizzo di un puntatore a una struttura di [**\_ elementi KSMULTIPLE**](ksmultiple-item.md) .</span><span class="sxs-lookup"><span data-stu-id="1f9d0-108">Address of a pointer to a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f9d0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f9d0-109">Return value</span></span>

<span data-ttu-id="1f9d0-110">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1f9d0-110">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="1f9d0-111">Se ha esito negativo, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f9d0-111">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f9d0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f9d0-112">Remarks</span></span>

<span data-ttu-id="1f9d0-113">Questo metodo restituisce una struttura di [**\_ elementi KSMULTIPLE**](ksmultiple-item.md) allocata dall'attività, che è seguita da zero o più strutture [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) .</span><span class="sxs-lookup"><span data-stu-id="1f9d0-113">This method returns a task-allocated [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, which is followed by zero or more [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structures.</span></span> <span data-ttu-id="1f9d0-114">Il membro **count** della struttura **dell' \_ elemento KSMULTIPLE** specifica il numero di strutture **REGPINMEDIUM** .</span><span class="sxs-lookup"><span data-stu-id="1f9d0-114">The **Count** member of the **KSMULTIPLE\_ITEM** structure specifies the number of **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="1f9d0-115">Ogni struttura **REGPINMEDIUM** definisce un supporto supportato dal pin.</span><span class="sxs-lookup"><span data-stu-id="1f9d0-115">Each **REGPINMEDIUM** structure defines a medium supported by the pin.</span></span>

<span data-ttu-id="1f9d0-116">Il chiamante deve liberare le strutture restituite, usando la funzione **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="1f9d0-116">The caller must free the returned structures, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="1f9d0-117">Prima di ksproxy. h, è necessario includere KS. h.</span><span class="sxs-lookup"><span data-stu-id="1f9d0-117">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="1f9d0-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="1f9d0-118">Examples</span></span>

<span data-ttu-id="1f9d0-119">La funzione helper seguente tenta di trovare una corrispondenza con un pin rispetto a un supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="1f9d0-119">The following helper function attempts to match a pin against a specified medium.</span></span>


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="1f9d0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f9d0-120">Requirements</span></span>



| <span data-ttu-id="1f9d0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f9d0-121">Requirement</span></span> | <span data-ttu-id="1f9d0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1f9d0-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9d0-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f9d0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1f9d0-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1f9d0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1f9d0-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f9d0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1f9d0-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1f9d0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f9d0-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f9d0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f9d0-128"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f9d0-128"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="1f9d0-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="1f9d0-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f9d0-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f9d0-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f9d0-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f9d0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9d0-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="1f9d0-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="1f9d0-133">**Interfaccia IKsPin**</span><span class="sxs-lookup"><span data-stu-id="1f9d0-133">**IKsPin Interface**</span></span>](ikspin.md)
</dt> <dt>

[<span data-ttu-id="1f9d0-134">Filtri driver di classe WDM</span><span class="sxs-lookup"><span data-stu-id="1f9d0-134">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
</dt> </dl>

 

 




