---
description: GUID dell'applicazione del Sottoscrittore.
ms.assetid: 46c91cae-ca31-4eac-baa8-d36910917f0f
title: 'Proprietà IEventSubscription3:: SubscriberApplicationID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberApplicationID
- IEventSubscription3.get_SubscriberApplicationID
- IEventSubscription3.put_SubscriberApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: c2e726d97821a7a7143f4971a4918227235adb9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225613"
---
# <a name="ieventsubscription3subscriberapplicationid-property"></a><span data-ttu-id="7aa5b-103">Proprietà IEventSubscription3:: SubscriberApplicationID</span><span class="sxs-lookup"><span data-stu-id="7aa5b-103">IEventSubscription3::SubscriberApplicationID property</span></span>

<span data-ttu-id="7aa5b-104">GUID dell'applicazione del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="7aa5b-104">The application GUID of the subscriber.</span></span>

<span data-ttu-id="7aa5b-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7aa5b-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aa5b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7aa5b-106">Syntax</span></span>


```C++
HRESULT put_SubscriberApplicationID(
  [in]          BSTR bstrSubscriberApplicationID
);

HRESULT get_SubscriberApplicationID(
  [out, retval] BSTR *pbstrSubscriberApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="7aa5b-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7aa5b-107">Property value</span></span>

<span data-ttu-id="7aa5b-108">Stringa che contiene il GUID dell'applicazione del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="7aa5b-108">A string containing the GUID of the subscriber application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7aa5b-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7aa5b-109">Error codes</span></span>

<span data-ttu-id="7aa5b-110">Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto, e ha \_ esito negativo e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7aa5b-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aa5b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7aa5b-111">Requirements</span></span>



| <span data-ttu-id="7aa5b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aa5b-112">Requirement</span></span> | <span data-ttu-id="7aa5b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7aa5b-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7aa5b-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7aa5b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7aa5b-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7aa5b-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7aa5b-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7aa5b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7aa5b-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7aa5b-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7aa5b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7aa5b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aa5b-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="7aa5b-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




