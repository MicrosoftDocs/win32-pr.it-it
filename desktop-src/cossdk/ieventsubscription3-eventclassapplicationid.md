---
description: GUID dell'applicazione dell'oggetto della classe di evento.
ms.assetid: 0d19183a-429c-4564-b6a5-f06481d27e00
title: 'Proprietà IEventSubscription3:: EventClassApplicationID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassApplicationID
- IEventSubscription3.get_EventClassApplicationID
- IEventSubscription3.put_EventClassApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e80a8d8f557c80a1b2605328728260eb8ae7bd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127030"
---
# <a name="ieventsubscription3eventclassapplicationid-property"></a><span data-ttu-id="f92d3-103">Proprietà IEventSubscription3:: EventClassApplicationID</span><span class="sxs-lookup"><span data-stu-id="f92d3-103">IEventSubscription3::EventClassApplicationID property</span></span>

<span data-ttu-id="f92d3-104">GUID dell'applicazione dell'oggetto della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="f92d3-104">The application GUID of the event class object.</span></span>

<span data-ttu-id="f92d3-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f92d3-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f92d3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f92d3-106">Syntax</span></span>


```C++
HRESULT put_EventClassApplicationID(
  [in]          BSTR bstrEventClassApplicationID
);

HRESULT get_EventClassApplicationID(
  [out, retval] BSTR *pbstrEventClassApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="f92d3-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f92d3-107">Property value</span></span>

<span data-ttu-id="f92d3-108">Stringa che contiene il GUID dell'applicazione della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="f92d3-108">A string containing the GUID of the event class application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f92d3-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f92d3-109">Error codes</span></span>

<span data-ttu-id="f92d3-110">Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto, e ha \_ esito negativo e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f92d3-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="f92d3-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f92d3-111">Requirements</span></span>



| <span data-ttu-id="f92d3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f92d3-112">Requirement</span></span> | <span data-ttu-id="f92d3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f92d3-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f92d3-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f92d3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f92d3-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f92d3-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f92d3-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f92d3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f92d3-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f92d3-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f92d3-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f92d3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f92d3-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="f92d3-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




