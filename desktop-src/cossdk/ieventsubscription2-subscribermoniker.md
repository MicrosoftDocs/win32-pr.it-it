---
description: Moniker dei sottoscrittori.
ms.assetid: d33d8c80-3251-4ec7-9cf3-d0b60d91ed5a
title: Proprietà IEventSubscription2SubscriberMoniker
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.SubscriberMoniker
- IEventSubscription2.get_SubscriberMoniker
- IEventSubscription2.put_SubscriberMoniker
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9496a3046b4bb0e99a88322892e557588a92aab8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748303"
---
# <a name="ieventsubscription2subscribermoniker-property"></a><span data-ttu-id="62617-103">Proprietà IEventSubscription2:: SubscriberMoniker</span><span class="sxs-lookup"><span data-stu-id="62617-103">IEventSubscription2::SubscriberMoniker property</span></span>

<span data-ttu-id="62617-104">Moniker del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="62617-104">The subscriber's moniker.</span></span>

<span data-ttu-id="62617-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="62617-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="62617-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62617-106">Syntax</span></span>


```C++
HRESULT put_SubscriberMoniker(
  [in]          BSTR bstrMoniker
);

HRESULT get_SubscriberMoniker(
  [out, retval] BSTR *pbstrMoniker
);
```



## <a name="property-value"></a><span data-ttu-id="62617-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="62617-107">Property value</span></span>

<span data-ttu-id="62617-108">Stringa del moniker che specifica il Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="62617-108">A moniker string specifying the subscriber.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62617-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="62617-109">Error codes</span></span>

<span data-ttu-id="62617-110">Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto, e ha \_ esito negativo e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62617-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="62617-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62617-111">Requirements</span></span>



| <span data-ttu-id="62617-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="62617-112">Requirement</span></span> | <span data-ttu-id="62617-113">Valore</span><span class="sxs-lookup"><span data-stu-id="62617-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="62617-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62617-114">Minimum supported client</span></span><br/> | <span data-ttu-id="62617-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62617-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="62617-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62617-116">Minimum supported server</span></span><br/> | <span data-ttu-id="62617-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62617-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="62617-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62617-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62617-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="62617-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




