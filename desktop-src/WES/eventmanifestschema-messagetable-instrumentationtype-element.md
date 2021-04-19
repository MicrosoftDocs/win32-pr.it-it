---
title: Elemento messageTable (EventsType)
description: Contiene un riferimento a una stringa nella sezione localizzazione del manifesto. | Elemento messageTable (EventsType)
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- EventLog elemento messageTable
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85ce478fb30389ba911ef9dd76473a6261974f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321285"
---
# <a name="messagetable-eventstype-element"></a><span data-ttu-id="208a9-105">Elemento messageTable (EventsType)</span><span class="sxs-lookup"><span data-stu-id="208a9-105">messageTable (EventsType) Element</span></span>

<span data-ttu-id="208a9-106">Contiene un riferimento a una stringa nella sezione localizzazione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="208a9-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:attribute name="value"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="mid"
                        type="string"
                        use="optional"
                     />
                    <xs:attribute name="message"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="symbol"
                        type="string"
                        use="optional"
                     />
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="208a9-107">L'elemento **messageTable** è definito dal tipo complesso [**EventsType**](eventmanifestschema-eventstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="208a9-107">The **messageTable** element is defined by the [**EventsType**](eventmanifestschema-eventstype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="208a9-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="208a9-108">Child elements</span></span>



| <span data-ttu-id="208a9-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="208a9-109">Element</span></span>                                                             | <span data-ttu-id="208a9-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="208a9-110">Type</span></span> | <span data-ttu-id="208a9-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="208a9-111">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="208a9-112">**message**</span><span class="sxs-lookup"><span data-stu-id="208a9-112">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="208a9-113">Specifica un riferimento a una stringa nella sezione localizzazione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="208a9-113">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="208a9-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="208a9-114">Attributes</span></span>



| <span data-ttu-id="208a9-115">Nome</span><span class="sxs-lookup"><span data-stu-id="208a9-115">Name</span></span>    | <span data-ttu-id="208a9-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="208a9-116">Type</span></span>   | <span data-ttu-id="208a9-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="208a9-117">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208a9-118">message</span><span class="sxs-lookup"><span data-stu-id="208a9-118">message</span></span> | <span data-ttu-id="208a9-119">string</span><span class="sxs-lookup"><span data-stu-id="208a9-119">string</span></span> | <span data-ttu-id="208a9-120">Riferimento alla stringa localizzata nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="208a9-120">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="208a9-121">mid</span><span class="sxs-lookup"><span data-stu-id="208a9-121">mid</span></span>     | <span data-ttu-id="208a9-122">string</span><span class="sxs-lookup"><span data-stu-id="208a9-122">string</span></span> | <span data-ttu-id="208a9-123">Non usato.</span><span class="sxs-lookup"><span data-stu-id="208a9-123">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="208a9-124">simbolo</span><span class="sxs-lookup"><span data-stu-id="208a9-124">symbol</span></span>  | <span data-ttu-id="208a9-125">string</span><span class="sxs-lookup"><span data-stu-id="208a9-125">string</span></span> | <span data-ttu-id="208a9-126">Nome simbolico che si desidera venga creato dal compilatore di messaggi per questa stringa di messaggio.</span><span class="sxs-lookup"><span data-stu-id="208a9-126">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="208a9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="208a9-127">value</span></span>   | <span data-ttu-id="208a9-128">string</span><span class="sxs-lookup"><span data-stu-id="208a9-128">string</span></span> | <span data-ttu-id="208a9-129">Numero da utilizzare come identificatore del messaggio per questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="208a9-129">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="208a9-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="208a9-130">Requirements</span></span>



| <span data-ttu-id="208a9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="208a9-131">Requirement</span></span> | <span data-ttu-id="208a9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="208a9-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="208a9-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="208a9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="208a9-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="208a9-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="208a9-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="208a9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="208a9-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="208a9-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="208a9-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="208a9-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="208a9-138">**Elementi padre**</span><span class="sxs-lookup"><span data-stu-id="208a9-138">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="208a9-139">**Elemento Events (InstrumentationType)**</span><span class="sxs-lookup"><span data-stu-id="208a9-139">**events (InstrumentationType) Element**</span></span>](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





