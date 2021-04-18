---
title: Message (messageTable)-elemento
description: Contiene un riferimento a una stringa nella sezione localizzazione del manifesto. | Message (messageTable)-elemento
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- EventLog elemento messaggio
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321286"
---
# <a name="message-messagetable-element"></a><span data-ttu-id="f1171-105">Message (messageTable)-elemento</span><span class="sxs-lookup"><span data-stu-id="f1171-105">message (messageTable) Element</span></span>

<span data-ttu-id="f1171-106">Contiene un riferimento a una stringa nella sezione localizzazione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="f1171-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="message">
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
```

<span data-ttu-id="f1171-107">L'elemento **Message** è definito dall'elemento [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f1171-107">The **message** element is defined by the [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="f1171-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="f1171-108">Attributes</span></span>



| <span data-ttu-id="f1171-109">Nome</span><span class="sxs-lookup"><span data-stu-id="f1171-109">Name</span></span>    | <span data-ttu-id="f1171-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1171-110">Type</span></span>   | <span data-ttu-id="f1171-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1171-111">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1171-112">message</span><span class="sxs-lookup"><span data-stu-id="f1171-112">message</span></span> | <span data-ttu-id="f1171-113">string</span><span class="sxs-lookup"><span data-stu-id="f1171-113">string</span></span> | <span data-ttu-id="f1171-114">Riferimento alla stringa localizzata nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="f1171-114">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="f1171-115">mid</span><span class="sxs-lookup"><span data-stu-id="f1171-115">mid</span></span>     | <span data-ttu-id="f1171-116">string</span><span class="sxs-lookup"><span data-stu-id="f1171-116">string</span></span> | <span data-ttu-id="f1171-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f1171-117">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="f1171-118">simbolo</span><span class="sxs-lookup"><span data-stu-id="f1171-118">symbol</span></span>  | <span data-ttu-id="f1171-119">string</span><span class="sxs-lookup"><span data-stu-id="f1171-119">string</span></span> | <span data-ttu-id="f1171-120">Nome simbolico che si desidera venga creato dal compilatore di messaggi per questa stringa di messaggio.</span><span class="sxs-lookup"><span data-stu-id="f1171-120">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="f1171-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f1171-121">value</span></span>   | <span data-ttu-id="f1171-122">string</span><span class="sxs-lookup"><span data-stu-id="f1171-122">string</span></span> | <span data-ttu-id="f1171-123">Numero da utilizzare come identificatore del messaggio per questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="f1171-123">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="f1171-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1171-124">Requirements</span></span>



| <span data-ttu-id="f1171-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1171-125">Requirement</span></span> | <span data-ttu-id="f1171-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f1171-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1171-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1171-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f1171-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1171-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1171-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1171-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f1171-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1171-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1171-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1171-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1171-132">**Elementi padre**</span><span class="sxs-lookup"><span data-stu-id="f1171-132">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="f1171-133">**messageTable (EventsType)**</span><span class="sxs-lookup"><span data-stu-id="f1171-133">**messageTable (EventsType)**</span></span>](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[<span data-ttu-id="f1171-134">**messageTable (MetadataType)**</span><span class="sxs-lookup"><span data-stu-id="f1171-134">**messageTable (MetadataType)**</span></span>](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





