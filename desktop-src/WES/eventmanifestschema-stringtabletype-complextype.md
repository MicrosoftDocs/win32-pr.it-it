---
title: Tipo complesso StringTableType
description: Definisce un elenco di stringhe localizzate a cui è possibile fare riferimento nel manifesto. | Tipo complesso StringTableType
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- Log eventi di tipo complesso StringTableType
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321606"
---
# <a name="stringtabletype-complex-type"></a><span data-ttu-id="06480-105">Tipo complesso StringTableType</span><span class="sxs-lookup"><span data-stu-id="06480-105">StringTableType Complex Type</span></span>

<span data-ttu-id="06480-106">Definisce un elenco di stringhe localizzate a cui è possibile fare riferimento nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="06480-106">Defines a list of localized strings that you can reference in your manifest.</span></span>

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="06480-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="06480-107">Child elements</span></span>



| <span data-ttu-id="06480-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="06480-108">Element</span></span>                                                              | <span data-ttu-id="06480-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="06480-109">Type</span></span> | <span data-ttu-id="06480-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06480-110">Description</span></span>                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [<span data-ttu-id="06480-111">**string**</span><span class="sxs-lookup"><span data-stu-id="06480-111">**string**</span></span>](eventmanifestschema-string-stringtabletype-element.md) |      | <span data-ttu-id="06480-112">Definisce una stringa localizzata.</span><span class="sxs-lookup"><span data-stu-id="06480-112">Defines a localized string.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="06480-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="06480-113">Attributes</span></span>



| <span data-ttu-id="06480-114">Nome</span><span class="sxs-lookup"><span data-stu-id="06480-114">Name</span></span>       | <span data-ttu-id="06480-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="06480-115">Type</span></span>   | <span data-ttu-id="06480-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06480-116">Description</span></span>                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06480-117">id</span><span class="sxs-lookup"><span data-stu-id="06480-117">id</span></span>         | <span data-ttu-id="06480-118">string</span><span class="sxs-lookup"><span data-stu-id="06480-118">string</span></span> | <span data-ttu-id="06480-119">Identificatore che identifica in modo univoco la stringa nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="06480-119">An identifier that uniquely identifies the string within the string table.</span></span> <span data-ttu-id="06480-120">Ad esempio, "Printer. Connection".</span><span class="sxs-lookup"><span data-stu-id="06480-120">For example, "Printer.Connection".</span></span><br/> |
| <span data-ttu-id="06480-121">stringType</span><span class="sxs-lookup"><span data-stu-id="06480-121">stringType</span></span> | <span data-ttu-id="06480-122">string</span><span class="sxs-lookup"><span data-stu-id="06480-122">string</span></span> | <span data-ttu-id="06480-123">Non usato.</span><span class="sxs-lookup"><span data-stu-id="06480-123">Not used.</span></span><br/>                                                                                                     |
| <span data-ttu-id="06480-124">Valore</span><span class="sxs-lookup"><span data-stu-id="06480-124">value</span></span>      | <span data-ttu-id="06480-125">string</span><span class="sxs-lookup"><span data-stu-id="06480-125">string</span></span> | <span data-ttu-id="06480-126">Stringa localizzata.</span><span class="sxs-lookup"><span data-stu-id="06480-126">The localized string.</span></span><br/>                                                                                         |



## <a name="remarks"></a><span data-ttu-id="06480-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="06480-127">Remarks</span></span>

<span data-ttu-id="06480-128">È possibile fare riferimento alle stringhe da qualsiasi tipo di manifesto che contiene l'attributo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="06480-128">You can reference the strings from any manifest type that contains the message attribute.</span></span> <span data-ttu-id="06480-129">Per fare riferimento a una stringa con un stringType di "String" e un ID "Printer. Connection", usare $ (String. Printer. Connection) come valore dell'attributo Message.</span><span class="sxs-lookup"><span data-stu-id="06480-129">To reference a string with a stringType of "string" and an id of "Printer.Connection", use $(string.Printer.Connection) as the value of the message attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="06480-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06480-130">Requirements</span></span>



| <span data-ttu-id="06480-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="06480-131">Requirement</span></span> | <span data-ttu-id="06480-132">Valore</span><span class="sxs-lookup"><span data-stu-id="06480-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="06480-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06480-133">Minimum supported client</span></span><br/> | <span data-ttu-id="06480-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06480-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="06480-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06480-135">Minimum supported server</span></span><br/> | <span data-ttu-id="06480-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06480-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





