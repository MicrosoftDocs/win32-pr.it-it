---
description: Criteri di filtro che governano la sottoscrizione.
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: 'Proprietà IEventSubscription2:: FilterCriteria'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1443a89433cff91a298e8c390fce8f1f64b99f1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127407"
---
# <a name="ieventsubscription2filtercriteria-property"></a><span data-ttu-id="78a71-103">Proprietà IEventSubscription2:: FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="78a71-103">IEventSubscription2::FilterCriteria property</span></span>

<span data-ttu-id="78a71-104">Criteri di filtro che governano la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="78a71-104">The filter criteria governing the subscription.</span></span>

<span data-ttu-id="78a71-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="78a71-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="78a71-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78a71-106">Syntax</span></span>


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a><span data-ttu-id="78a71-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="78a71-107">Property value</span></span>

<span data-ttu-id="78a71-108">Criteri di filtro o CLSID per una classe che implementa [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span><span class="sxs-lookup"><span data-stu-id="78a71-108">The filter criteria or the CLSID for a class implementing [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span></span>

## <a name="error-codes"></a><span data-ttu-id="78a71-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="78a71-109">Error codes</span></span>

<span data-ttu-id="78a71-110">Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto, e ha \_ esito negativo e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="78a71-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="78a71-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78a71-111">Requirements</span></span>



| <span data-ttu-id="78a71-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="78a71-112">Requirement</span></span> | <span data-ttu-id="78a71-113">Valore</span><span class="sxs-lookup"><span data-stu-id="78a71-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="78a71-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78a71-114">Minimum supported client</span></span><br/> | <span data-ttu-id="78a71-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="78a71-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="78a71-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78a71-116">Minimum supported server</span></span><br/> | <span data-ttu-id="78a71-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="78a71-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="78a71-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78a71-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a71-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="78a71-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




