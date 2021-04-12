---
description: Novità di Windows 7. Identifica una proprietà correlata alla proprietà definita nel file di descrizione della proprietà.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344801"
---
# <a name="relatedproperty"></a><span data-ttu-id="665d8-104">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="665d8-104">relatedProperty</span></span>

<span data-ttu-id="665d8-105">Novità di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="665d8-105">New for Windows 7.</span></span> <span data-ttu-id="665d8-106">Identifica una proprietà correlata alla proprietà definita nel file di descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="665d8-106">Identifies a property that is related to the property defined in the property description file.</span></span> <span data-ttu-id="665d8-107">È possibile che siano presenti tutti gli elementi [relatedProperty]() all'interno di un [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="665d8-107">There can be as many [relatedProperty]() elements within a [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="665d8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="665d8-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="665d8-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="665d8-109">Element Information</span></span>



| <span data-ttu-id="665d8-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="665d8-110">Parent Element</span></span>                                                   | <span data-ttu-id="665d8-111">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="665d8-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="665d8-112">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="665d8-112">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) | <span data-ttu-id="665d8-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="665d8-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="665d8-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="665d8-114">Attributes</span></span>



| <span data-ttu-id="665d8-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="665d8-115">Attribute</span></span>        | <span data-ttu-id="665d8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="665d8-116">Description</span></span>                                                        |
|------------------|--------------------------------------------------------------------|
| <span data-ttu-id="665d8-117">relationshipName</span><span class="sxs-lookup"><span data-stu-id="665d8-117">relationshipName</span></span> | <span data-ttu-id="665d8-118">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="665d8-118">Public.</span></span> <span data-ttu-id="665d8-119">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="665d8-119">Required.</span></span> <span data-ttu-id="665d8-120">Nome canonico della relazione di proprietà.</span><span class="sxs-lookup"><span data-stu-id="665d8-120">The canonical name of the property relationship.</span></span> |
| <span data-ttu-id="665d8-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="665d8-121">propertyName</span></span>     | <span data-ttu-id="665d8-122">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="665d8-122">Public.</span></span> <span data-ttu-id="665d8-123">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="665d8-123">Required.</span></span> <span data-ttu-id="665d8-124">Nome canonico della proprietà correlata.</span><span class="sxs-lookup"><span data-stu-id="665d8-124">The canonical name of the related property.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="665d8-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="665d8-125">Remarks</span></span>

<span data-ttu-id="665d8-126">Questo elemento consente di eseguire il mapping di una proprietà a un'altra.</span><span class="sxs-lookup"><span data-stu-id="665d8-126">This element enables you to map one property to another.</span></span> <span data-ttu-id="665d8-127">Ad esempio, è possibile eseguire il mapping del testo della proprietà personalizzata fabrikam. StorageCapacity a System. Capacity:</span><span class="sxs-lookup"><span data-stu-id="665d8-127">For example, you can map the text of your custom property, Fabrikam.StorageCapacity, to System.Capacity:</span></span>


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
