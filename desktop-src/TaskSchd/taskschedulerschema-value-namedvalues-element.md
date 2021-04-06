---
title: Valore (namedValues) (elemento)
description: Contiene il valore associato a un nome in una coppia nome-valore.
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- Elemento Value Utilità di pianificazione
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743319"
---
# <a name="value-namedvalues-element"></a><span data-ttu-id="9152a-104">Valore (namedValues) (elemento)</span><span class="sxs-lookup"><span data-stu-id="9152a-104">Value (namedValues) Element</span></span>

<span data-ttu-id="9152a-105">Contiene il valore associato a un nome in una coppia nome-valore.</span><span class="sxs-lookup"><span data-stu-id="9152a-105">Contains the value that is associated with a name in a name-value pair.</span></span>

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

<span data-ttu-id="9152a-106">L'elemento **value** è definito dal tipo complesso [**namedValues**](taskschedulerschema-namedvalues-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9152a-106">The **Value** element is defined by the [**namedValues**](taskschedulerschema-namedvalues-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9152a-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="9152a-107">Parent element</span></span>



| <span data-ttu-id="9152a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9152a-108">Element</span></span>                                                                                              | <span data-ttu-id="9152a-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="9152a-109">Derived from</span></span>                                                       | <span data-ttu-id="9152a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9152a-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9152a-111">**ValueQueries (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="9152a-111">**ValueQueries (eventTriggerType)**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="9152a-112">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="9152a-112">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md) | <span data-ttu-id="9152a-113">Specifica una raccolta di query XPath denominate.</span><span class="sxs-lookup"><span data-stu-id="9152a-113">Specifies a collection of named XPath queries.</span></span> <span data-ttu-id="9152a-114">Ogni query della raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata nell'elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9152a-114">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="9152a-115">Il nome della query può essere utilizzato come variabile nel messaggio di un'azione ShowMessage.</span><span class="sxs-lookup"><span data-stu-id="9152a-115">The name of the query can be used as a variable in the message of a ShowMessage action.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9152a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9152a-116">Remarks</span></span>

<span data-ttu-id="9152a-117">Per lo sviluppo in C++, vedere [**proprietà Value di ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span><span class="sxs-lookup"><span data-stu-id="9152a-117">For C++ development, see [**Value Property of ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span></span>

<span data-ttu-id="9152a-118">Per lo sviluppo di script, vedere [**TaskNamedValuePair. Value**](tasknamedvaluepair-value.md).</span><span class="sxs-lookup"><span data-stu-id="9152a-118">For script development, see [**TaskNamedValuePair.Value**](tasknamedvaluepair-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9152a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9152a-119">Requirements</span></span>



| <span data-ttu-id="9152a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9152a-120">Requirement</span></span> | <span data-ttu-id="9152a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9152a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9152a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9152a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9152a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9152a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9152a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9152a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9152a-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9152a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





