---
title: Tipo complesso NamedQueryType
description: Non usato. Definisce un elenco di query denominate che eseguono una query sulla stringa del messaggio di evento per un valore ed eseguono un'azione specificata, se trovata. | Tipo complesso NamedQueryType
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- Log eventi di tipo complesso NamedQueryType
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321626"
---
# <a name="namedquerytype-complex-type"></a><span data-ttu-id="07eb2-106">Tipo complesso NamedQueryType</span><span class="sxs-lookup"><span data-stu-id="07eb2-106">NamedQueryType Complex Type</span></span>

<span data-ttu-id="07eb2-107">Non usato.</span><span class="sxs-lookup"><span data-stu-id="07eb2-107">Not used.</span></span> <span data-ttu-id="07eb2-108">Definisce un elenco di query denominate che eseguono una query sulla stringa del messaggio di evento per un valore ed eseguono un'azione specificata, se trovata.</span><span class="sxs-lookup"><span data-stu-id="07eb2-108">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span>

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="07eb2-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="07eb2-109">Child elements</span></span>



| <span data-ttu-id="07eb2-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="07eb2-110">Element</span></span>                                                                       | <span data-ttu-id="07eb2-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="07eb2-111">Type</span></span>                                                                             | <span data-ttu-id="07eb2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07eb2-112">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07eb2-113">**patternMaps**</span><span class="sxs-lookup"><span data-stu-id="07eb2-113">**patternMaps**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md) | [<span data-ttu-id="07eb2-114">**PatternMapListType**</span><span class="sxs-lookup"><span data-stu-id="07eb2-114">**PatternMapListType**</span></span>](eventmanifestschema-patternmaplisttype-complextype.md) | <span data-ttu-id="07eb2-115">Definisce un elenco di coppie di espressioni regolari utilizzate per modificare la stringa del messaggio.</span><span class="sxs-lookup"><span data-stu-id="07eb2-115">Defines a list of regular expression pairs that are used to alter the message string.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="07eb2-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="07eb2-116">Examples</span></span>

<span data-ttu-id="07eb2-117">Nell'esempio seguente viene illustrato come utilizzare l'elemento [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="07eb2-117">The following example shows how to use the [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) element.</span></span> <span data-ttu-id="07eb2-118">Questo esempio accetta il contenuto della stringa del messaggio e lo inserisce nella stringa https://www .*MessageString*. com.</span><span class="sxs-lookup"><span data-stu-id="07eb2-118">This example takes the contents of the message string and inserts it into the string https://www.*messagestring*.com.</span></span> <span data-ttu-id="07eb2-119">Sostituisce quindi la stringa del messaggio con il risultato.</span><span class="sxs-lookup"><span data-stu-id="07eb2-119">It then replaces the message string with the result.</span></span> <span data-ttu-id="07eb2-120">Se, ad esempio, la stringa del messaggio contiene Microsoft, la query sostituirà la stringa di messaggio Microsoft con https://www.Microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="07eb2-120">For example, if the message string contained Microsoft, the query would replace the Microsoft message string with https://www.Microsoft.com.</span></span>


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a><span data-ttu-id="07eb2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07eb2-121">Requirements</span></span>



| <span data-ttu-id="07eb2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="07eb2-122">Requirement</span></span> | <span data-ttu-id="07eb2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="07eb2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07eb2-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07eb2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="07eb2-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07eb2-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07eb2-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07eb2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="07eb2-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07eb2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





