---
description: GUID della partizione dell'oggetto della classe di evento.
ms.assetid: 154849ac-350c-4b2f-bb51-ac6973f0a8fa
title: 'Proprietà IEventSubscription3:: EventClassPartitionID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassPartitionID
- IEventSubscription3.get_EventClassPartitionID
- IEventSubscription3.put_EventClassPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: d41d3e2a170deffb73f1f533226421d88f150c01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524202"
---
# <a name="ieventsubscription3eventclasspartitionid-property"></a><span data-ttu-id="a4825-103">Proprietà IEventSubscription3:: EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="a4825-103">IEventSubscription3::EventClassPartitionID property</span></span>

<span data-ttu-id="a4825-104">GUID della partizione dell'oggetto della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="a4825-104">The partition GUID of the event class object.</span></span>

<span data-ttu-id="a4825-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a4825-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4825-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4825-106">Syntax</span></span>


```C++
HRESULT put_EventClassPartitionID(
  [in]          BSTR bstrEventClassPartitionID
);

HRESULT get_EventClassPartitionID(
  [out, retval] BSTR *pbstrEventClassPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="a4825-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a4825-107">Property value</span></span>

<span data-ttu-id="a4825-108">Stringa contenente il GUID della partizione della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="a4825-108">A string containing the GUID of the event class partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a4825-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a4825-109">Error codes</span></span>

<span data-ttu-id="a4825-110">Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto, e ha \_ esito negativo e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a4825-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4825-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4825-111">Requirements</span></span>



| <span data-ttu-id="a4825-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4825-112">Requirement</span></span> | <span data-ttu-id="a4825-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a4825-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a4825-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4825-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a4825-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a4825-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a4825-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4825-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a4825-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a4825-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a4825-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4825-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4825-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="a4825-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




