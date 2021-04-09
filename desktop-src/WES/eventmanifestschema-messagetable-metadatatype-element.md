---
title: Elemento messageTable (MetadataType)
description: Contiene riferimenti alle stringhe utilizzate nella sezione relativa ai metadati del manifesto di strumentazione eventi. Le stringhe vengono archiviate in un gruppo di elementi messaggio e ID abbinati.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
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
ms.openlocfilehash: eb5efc261a2c055a95f71ba556c9acbc0ad45373
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119187"
---
# <a name="messagetable-metadatatype-element"></a><span data-ttu-id="a1397-105">Elemento messageTable (MetadataType)</span><span class="sxs-lookup"><span data-stu-id="a1397-105">messageTable (MetadataType) Element</span></span>

<span data-ttu-id="a1397-106">Contiene riferimenti alle stringhe utilizzate nella sezione relativa ai metadati del manifesto di strumentazione eventi.</span><span class="sxs-lookup"><span data-stu-id="a1397-106">Contains references to strings that are used in the event instrumentation manifest metadata section.</span></span> <span data-ttu-id="a1397-107">Le stringhe vengono archiviate in un gruppo di elementi [**messaggio**](eventmanifestschema-message-messagetable-element.md) e ID abbinati.</span><span class="sxs-lookup"><span data-stu-id="a1397-107">The strings are stored in a group of [**message**](eventmanifestschema-message-messagetable-element.md) elements and IDs paired together.</span></span>

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

<span data-ttu-id="a1397-108">L'elemento **messageTable** è definito dal tipo complesso [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a1397-108">The **messageTable** element is defined by the [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a1397-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a1397-109">Child elements</span></span>



| <span data-ttu-id="a1397-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="a1397-110">Element</span></span>                                                             | <span data-ttu-id="a1397-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1397-111">Type</span></span> | <span data-ttu-id="a1397-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1397-112">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1397-113">**message**</span><span class="sxs-lookup"><span data-stu-id="a1397-113">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="a1397-114">Specifica un riferimento a una stringa nella sezione localizzazione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="a1397-114">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="a1397-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="a1397-115">Attributes</span></span>



| <span data-ttu-id="a1397-116">Nome</span><span class="sxs-lookup"><span data-stu-id="a1397-116">Name</span></span>    | <span data-ttu-id="a1397-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1397-117">Type</span></span>   | <span data-ttu-id="a1397-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1397-118">Description</span></span>                                                              |
|---------|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="a1397-119">message</span><span class="sxs-lookup"><span data-stu-id="a1397-119">message</span></span> | <span data-ttu-id="a1397-120">string</span><span class="sxs-lookup"><span data-stu-id="a1397-120">string</span></span> | <span data-ttu-id="a1397-121">Riferimento alla stringa localizzata nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="a1397-121">A reference to the localized string in the string table.</span></span><br/>      |
| <span data-ttu-id="a1397-122">mid</span><span class="sxs-lookup"><span data-stu-id="a1397-122">mid</span></span>     | <span data-ttu-id="a1397-123">string</span><span class="sxs-lookup"><span data-stu-id="a1397-123">string</span></span> | <span data-ttu-id="a1397-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a1397-124">Not used.</span></span><br/>                                                     |
| <span data-ttu-id="a1397-125">simbolo</span><span class="sxs-lookup"><span data-stu-id="a1397-125">symbol</span></span>  | <span data-ttu-id="a1397-126">string</span><span class="sxs-lookup"><span data-stu-id="a1397-126">string</span></span> | <span data-ttu-id="a1397-127">Simbolo utilizzato per fare riferimento al messaggio.</span><span class="sxs-lookup"><span data-stu-id="a1397-127">The symbol used to reference the message.</span></span><br/>                     |
| <span data-ttu-id="a1397-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a1397-128">value</span></span>   | <span data-ttu-id="a1397-129">string</span><span class="sxs-lookup"><span data-stu-id="a1397-129">string</span></span> | <span data-ttu-id="a1397-130">Numero da utilizzare come identificatore del messaggio per questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a1397-130">The number to use as the message identifier for this message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a1397-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1397-131">Requirements</span></span>



| <span data-ttu-id="a1397-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1397-132">Requirement</span></span> | <span data-ttu-id="a1397-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a1397-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1397-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1397-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a1397-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1397-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1397-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1397-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a1397-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1397-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1397-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1397-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1397-139">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="a1397-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a1397-140">**MetadataType**</span><span class="sxs-lookup"><span data-stu-id="a1397-140">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

<span data-ttu-id="a1397-141">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="a1397-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a1397-142">**metadati (instrumentationManifest)**</span><span class="sxs-lookup"><span data-stu-id="a1397-142">**metadata (instrumentationManifest)**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





