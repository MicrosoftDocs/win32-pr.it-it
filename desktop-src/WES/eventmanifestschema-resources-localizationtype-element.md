---
title: Elemento resources (LocalizationType)
description: Definisce un gruppo di tabelle di stringhe che contengono le stringhe localizzate a cui si fa riferimento nel manifesto.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- elemento resources-EventLog
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55bdfe504da08c754c18b790e282eba6787c3ee3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300917"
---
# <a name="resources-localizationtype-element"></a><span data-ttu-id="343f7-104">Elemento resources (LocalizationType)</span><span class="sxs-lookup"><span data-stu-id="343f7-104">resources (LocalizationType) Element</span></span>

<span data-ttu-id="343f7-105">Definisce un gruppo di tabelle di stringhe che contengono le stringhe localizzate a cui si fa riferimento nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="343f7-105">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span>

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="343f7-106">L'elemento **Resources** viene definito dal tipo complesso [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="343f7-106">The **resources** element is defined by the [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="343f7-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="343f7-107">Child elements</span></span>



| <span data-ttu-id="343f7-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="343f7-108">Element</span></span>                                                                  | <span data-ttu-id="343f7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="343f7-109">Type</span></span>                                                                       | <span data-ttu-id="343f7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="343f7-110">Description</span></span>                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="343f7-111">**Un'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="343f7-111">**stringTable**</span></span>](eventmanifestschema-stringtable-resources-element.md) | [<span data-ttu-id="343f7-112">**StringTableType**</span><span class="sxs-lookup"><span data-stu-id="343f7-112">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="343f7-113">Definisce un elenco di stringhe localizzate a cui è possibile fare riferimento nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="343f7-113">Defines a list of localized strings that you can reference in your manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="343f7-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="343f7-114">Attributes</span></span>



| <span data-ttu-id="343f7-115">Nome</span><span class="sxs-lookup"><span data-stu-id="343f7-115">Name</span></span>    | <span data-ttu-id="343f7-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="343f7-116">Type</span></span>   | <span data-ttu-id="343f7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="343f7-117">Description</span></span>                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="343f7-118">culture</span><span class="sxs-lookup"><span data-stu-id="343f7-118">culture</span></span> | <span data-ttu-id="343f7-119">string</span><span class="sxs-lookup"><span data-stu-id="343f7-119">string</span></span> | <span data-ttu-id="343f7-120">Nome di linguaggio che identifica le impostazioni cultura delle stringhe localizzate nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="343f7-120">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="343f7-121">Ad esempio, "en-US" per l'inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="343f7-121">For example, "en-US" for English (United States).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="343f7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="343f7-122">Requirements</span></span>



| <span data-ttu-id="343f7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="343f7-123">Requirement</span></span> | <span data-ttu-id="343f7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="343f7-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="343f7-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="343f7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="343f7-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="343f7-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="343f7-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="343f7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="343f7-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="343f7-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="343f7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="343f7-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="343f7-130">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="343f7-130">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="343f7-131">**localizzazione (instrumentationManifest)**</span><span class="sxs-lookup"><span data-stu-id="343f7-131">**localization (instrumentationManifest)**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





