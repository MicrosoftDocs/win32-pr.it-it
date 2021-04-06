---
title: Elemento ValueQueries (eventTriggerType)
description: Contiene una sequenza di elementi ognuno dei quali contiene un nome e un valore di query XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- Utilità di pianificazione elemento ValueQueries
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963912"
---
# <a name="valuequeries-eventtriggertype-element"></a><span data-ttu-id="227fd-104">Elemento ValueQueries (eventTriggerType)</span><span class="sxs-lookup"><span data-stu-id="227fd-104">ValueQueries (eventTriggerType) Element</span></span>

<span data-ttu-id="227fd-105">Contiene una sequenza di elementi ognuno dei quali contiene un nome e un valore di query XPath.</span><span class="sxs-lookup"><span data-stu-id="227fd-105">Contains a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="227fd-106">Le query vengono applicate a un evento restituito dalla sottoscrizione dell'evento specificato nell'elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="227fd-106">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="227fd-107">Il nome del valore della query XPath può essere utilizzato come variabile nella sezione Action di un'attività.</span><span class="sxs-lookup"><span data-stu-id="227fd-107">The name for the XPath query value can be used as a variable in the action section of a task.</span></span>

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

<span data-ttu-id="227fd-108">L'elemento **ValueQueries** è definito dal tipo complesso [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="227fd-108">The **ValueQueries** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="227fd-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="227fd-109">Parent element</span></span>



| <span data-ttu-id="227fd-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="227fd-110">Element</span></span>                                                                                      | <span data-ttu-id="227fd-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="227fd-111">Derived from</span></span>                                                                 | <span data-ttu-id="227fd-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="227fd-112">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="227fd-113">**EventTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="227fd-113">**EventTrigger (triggerGroup)**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="227fd-114">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="227fd-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="227fd-115">Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="227fd-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="227fd-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="227fd-116">Remarks</span></span>

<span data-ttu-id="227fd-117">Per lo sviluppo in C++, vedere [**la proprietà ValueQueries di IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span><span class="sxs-lookup"><span data-stu-id="227fd-117">For C++ development, see [**ValueQueries Property of IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span></span>

<span data-ttu-id="227fd-118">Per lo sviluppo di script, vedere [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="227fd-118">For script development, see [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

## <a name="examples"></a><span data-ttu-id="227fd-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="227fd-119">Examples</span></span>

<span data-ttu-id="227fd-120">Per un esempio completo del codice XML per un'attività che specifica un trigger di evento usando questo elemento, vedere [esempio di trigger di evento (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="227fd-120">For a complete example of the XML for a task that specifies a an event trigger using this element, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="227fd-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="227fd-121">Requirements</span></span>



| <span data-ttu-id="227fd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="227fd-122">Requirement</span></span> | <span data-ttu-id="227fd-123">Valore</span><span class="sxs-lookup"><span data-stu-id="227fd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="227fd-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="227fd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="227fd-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="227fd-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="227fd-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="227fd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="227fd-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="227fd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

