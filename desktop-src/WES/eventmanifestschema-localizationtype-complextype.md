---
title: Tipo complesso LocalizationType
description: Definisce un gruppo di risorse localizzate a cui si fa riferimento nel manifesto. | Tipo complesso LocalizationType
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- Log eventi di tipo complesso LocalizationType
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbb6911ea606ea30d8e656f20b4c566d4f6d0e08
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321289"
---
# <a name="localizationtype-complex-type"></a><span data-ttu-id="4c90d-105">Tipo complesso LocalizationType</span><span class="sxs-lookup"><span data-stu-id="4c90d-105">LocalizationType Complex Type</span></span>

<span data-ttu-id="4c90d-106">Definisce un gruppo di risorse localizzate a cui si fa riferimento nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="4c90d-106">Defines a group of localized resources that you reference in your manifest.</span></span>

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4c90d-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4c90d-107">Child elements</span></span>



| <span data-ttu-id="4c90d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4c90d-108">Element</span></span>                                                                         | <span data-ttu-id="4c90d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c90d-109">Type</span></span>                                                                       | <span data-ttu-id="4c90d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c90d-110">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c90d-111">**risorse**</span><span class="sxs-lookup"><span data-stu-id="4c90d-111">**resources**</span></span>](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | <span data-ttu-id="4c90d-112">Definisce un gruppo di tabelle di stringhe che contengono le stringhe localizzate a cui si fa riferimento nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="4c90d-112">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span><br/> |
| [<span data-ttu-id="4c90d-113">**Un'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="4c90d-113">**stringTable**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md) | [<span data-ttu-id="4c90d-114">**StringTableType**</span><span class="sxs-lookup"><span data-stu-id="4c90d-114">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="4c90d-115">Definisce un elenco di stringhe localizzate a cui è possibile fare riferimento nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="4c90d-115">Defines a list of localized strings that you can reference in your manifest.</span></span><br/>                             |



## <a name="attributes"></a><span data-ttu-id="4c90d-116">Attributi</span><span class="sxs-lookup"><span data-stu-id="4c90d-116">Attributes</span></span>



| <span data-ttu-id="4c90d-117">Nome</span><span class="sxs-lookup"><span data-stu-id="4c90d-117">Name</span></span>            | <span data-ttu-id="4c90d-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c90d-118">Type</span></span>   | <span data-ttu-id="4c90d-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c90d-119">Description</span></span>                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c90d-120">culture</span><span class="sxs-lookup"><span data-stu-id="4c90d-120">culture</span></span>         | <span data-ttu-id="4c90d-121">string</span><span class="sxs-lookup"><span data-stu-id="4c90d-121">string</span></span> | <span data-ttu-id="4c90d-122">Nome di linguaggio che identifica le impostazioni cultura delle stringhe localizzate nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="4c90d-122">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="4c90d-123">Ad esempio, "en-US" per l'inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="4c90d-123">For example, "en-US" for English (United States).</span></span><br/> |
| <span data-ttu-id="4c90d-124">fallbackCulture</span><span class="sxs-lookup"><span data-stu-id="4c90d-124">fallbackCulture</span></span> | <span data-ttu-id="4c90d-125">string</span><span class="sxs-lookup"><span data-stu-id="4c90d-125">string</span></span> | <span data-ttu-id="4c90d-126">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4c90d-126">Not used.</span></span><br/>                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="4c90d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c90d-127">Requirements</span></span>



| <span data-ttu-id="4c90d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c90d-128">Requirement</span></span> | <span data-ttu-id="4c90d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4c90d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c90d-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c90d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4c90d-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c90d-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4c90d-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c90d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4c90d-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c90d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





