---
description: GUID della partizione del Sottoscrittore.
ms.assetid: 0b2411d3-cdc1-492c-a54f-ca3d3bd8b953
title: 'Proprietà IEventSubscription3:: SubscriberPartitionID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberPartitionID
- IEventSubscription3.get_SubscriberPartitionID
- IEventSubscription3.put_SubscriberPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: b09c41ac1b3a90c3275daf7afa0cd90fe2bb905c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225778"
---
# <a name="ieventsubscription3subscriberpartitionid-property"></a><span data-ttu-id="2d3f3-103">Proprietà IEventSubscription3:: SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="2d3f3-103">IEventSubscription3::SubscriberPartitionID property</span></span>

<span data-ttu-id="2d3f3-104">GUID della partizione del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="2d3f3-104">The partition GUID of the subscriber.</span></span>

<span data-ttu-id="2d3f3-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2d3f3-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d3f3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d3f3-106">Syntax</span></span>


```C++
HRESULT put_SubscriberPartitionID(
  [in]          BSTR bstrSubscriberPartitionID
);

HRESULT get_SubscriberPartitionID(
  [out, retval] BSTR *pbstrSubscriberPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="2d3f3-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2d3f3-107">Property value</span></span>

<span data-ttu-id="2d3f3-108">Stringa contenente il GUID della partizione del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="2d3f3-108">A string containing the GUID of the subscriber partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2d3f3-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2d3f3-109">Error codes</span></span>

<span data-ttu-id="2d3f3-110">Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto, e ha \_ esito negativo e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2d3f3-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d3f3-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d3f3-111">Requirements</span></span>



| <span data-ttu-id="2d3f3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d3f3-112">Requirement</span></span> | <span data-ttu-id="2d3f3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="2d3f3-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2d3f3-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d3f3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2d3f3-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d3f3-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2d3f3-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d3f3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2d3f3-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d3f3-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2d3f3-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d3f3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d3f3-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="2d3f3-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




