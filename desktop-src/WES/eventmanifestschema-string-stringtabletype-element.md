---
title: Elemento String (StringTableType)
description: Definisce una stringa localizzata.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- EventLog elemento stringa
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964407"
---
# <a name="string-stringtabletype-element"></a><span data-ttu-id="e7837-104">Elemento String (StringTableType)</span><span class="sxs-lookup"><span data-stu-id="e7837-104">string (StringTableType) Element</span></span>

<span data-ttu-id="e7837-105">Definisce una stringa localizzata.</span><span class="sxs-lookup"><span data-stu-id="e7837-105">Defines a localized string.</span></span>

``` syntax
<xs:element name="string">
    <xs:complexType>
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
```

<span data-ttu-id="e7837-106">L'elemento **String** è definito dal tipo complesso [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e7837-106">The **string** element is defined by the [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="e7837-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="e7837-107">Attributes</span></span>



| <span data-ttu-id="e7837-108">Nome</span><span class="sxs-lookup"><span data-stu-id="e7837-108">Name</span></span>       | <span data-ttu-id="e7837-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7837-109">Type</span></span>   | <span data-ttu-id="e7837-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7837-110">Description</span></span>                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7837-111">id</span><span class="sxs-lookup"><span data-stu-id="e7837-111">id</span></span>         | <span data-ttu-id="e7837-112">string</span><span class="sxs-lookup"><span data-stu-id="e7837-112">string</span></span> | <span data-ttu-id="e7837-113">Identificatore che identifica in modo univoco la stringa nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="e7837-113">An identifier that uniquely identifies the string within the string table.</span></span><br/> |
| <span data-ttu-id="e7837-114">stringType</span><span class="sxs-lookup"><span data-stu-id="e7837-114">stringType</span></span> | <span data-ttu-id="e7837-115">string</span><span class="sxs-lookup"><span data-stu-id="e7837-115">string</span></span> | <span data-ttu-id="e7837-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e7837-116">Not used.</span></span><br/>                                                                  |
| <span data-ttu-id="e7837-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e7837-117">value</span></span>      | <span data-ttu-id="e7837-118">string</span><span class="sxs-lookup"><span data-stu-id="e7837-118">string</span></span> | <span data-ttu-id="e7837-119">Stringa localizzata.</span><span class="sxs-lookup"><span data-stu-id="e7837-119">The localized string.</span></span><br/>                                                      |



## <a name="requirements"></a><span data-ttu-id="e7837-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7837-120">Requirements</span></span>



| <span data-ttu-id="e7837-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7837-121">Requirement</span></span> | <span data-ttu-id="e7837-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e7837-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7837-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7837-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e7837-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7837-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7837-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7837-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e7837-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7837-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7837-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7837-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7837-128">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="e7837-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="e7837-129">**Un'StringTable (LocalizationType)**</span><span class="sxs-lookup"><span data-stu-id="e7837-129">**stringTable (LocalizationType)**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





