---
description: Specifica un alias di ordinamento o un elenco di alias di ordinamento specificando un elemento che contiene una proprietà di ordinamento o un elenco di proprietà di ordinamento.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310130"
---
# <a name="aliasinfo"></a><span data-ttu-id="f0e0c-103">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="f0e0c-103">aliasInfo</span></span>

<span data-ttu-id="f0e0c-104">Specifica un alias di ordinamento o un elenco di alias di ordinamento specificando un elemento che contiene una proprietà di ordinamento o un elenco di proprietà di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="f0e0c-104">Specifies a sort alias or list of sort aliases by specifying an element that contains a sort property or list of sort properties.</span></span> <span data-ttu-id="f0e0c-105">Deve essere presente un solo elemento [aliasInfo]() per ogni elemento [PropertyDescription](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e0c-105">There should be only one [aliasInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span> <span data-ttu-id="f0e0c-106">Per le proprietà che impostano canGroupBy = true, a meno che non sia specificata una proprietà di ordinamento secondaria ( aliasInfo/@additionalSortByAliases = prop: example), l'utente può riscontrare un comportamento imprevisto quando si modifica il tipo di ordinamento in una vista raggruppata in base alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="f0e0c-106">For properties that set canGroupBy=true, unless a secondary sort property is specified (aliasInfo/@additionalSortByAliases=prop:example), the user may experience unexpected behavior when changing the sort order in a view that is grouped by the property.</span></span> <span data-ttu-id="f0e0c-107">In particolare, l'ordine dei gruppi cambierà, ma l'ordine degli elementi all'interno dei gruppi non lo è.</span><span class="sxs-lookup"><span data-stu-id="f0e0c-107">Specifically, the order of the groups will change, but the order of items within the groups will not.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e0c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0e0c-108">Syntax</span></span>


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="f0e0c-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f0e0c-109">Element Information</span></span>



| <span data-ttu-id="f0e0c-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="f0e0c-110">Parent Element</span></span>                                                   | <span data-ttu-id="f0e0c-111">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f0e0c-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="f0e0c-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f0e0c-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="f0e0c-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="f0e0c-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="f0e0c-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="f0e0c-114">Attributes</span></span>



| <span data-ttu-id="f0e0c-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="f0e0c-115">Attribute</span></span>               | <span data-ttu-id="f0e0c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0e0c-116">Description</span></span>                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e0c-117">sortByAlias</span><span class="sxs-lookup"><span data-stu-id="f0e0c-117">sortByAlias</span></span>             | <span data-ttu-id="f0e0c-118">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="f0e0c-118">Public.</span></span> <span data-ttu-id="f0e0c-119">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f0e0c-119">Optional.</span></span> <span data-ttu-id="f0e0c-120">Nome canonico della proprietà da utilizzare per l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="f0e0c-120">The canonical name of the property that should be used to sort by.</span></span> <span data-ttu-id="f0e0c-121">La stringa è di tipo canonico.</span><span class="sxs-lookup"><span data-stu-id="f0e0c-121">This string is of type canonical-type.</span></span>                                            |
| <span data-ttu-id="f0e0c-122">additionalSortByAliases</span><span class="sxs-lookup"><span data-stu-id="f0e0c-122">additionalSortByAliases</span></span> | <span data-ttu-id="f0e0c-123">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="f0e0c-123">Public.</span></span> <span data-ttu-id="f0e0c-124">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f0e0c-124">Optional.</span></span> <span data-ttu-id="f0e0c-125">Elenco delimitato da punti e virgola di proprietà aggiuntive da utilizzare durante l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="f0e0c-125">A semi-colon delimited list of additional properties to be used when sorting.</span></span> <span data-ttu-id="f0e0c-126">Le proprietà vengono applicate all'ordinamento nella sequenza specificata.</span><span class="sxs-lookup"><span data-stu-id="f0e0c-126">The properties are applied to the sort in the sequence they are given.</span></span> |



 

 

 
