---
description: Contenitore per uno o più elementi propertyDescription singoli.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310117"
---
# <a name="propertydescriptionlist"></a><span data-ttu-id="b9e2a-103">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="b9e2a-103">propertyDescriptionList</span></span>

<span data-ttu-id="b9e2a-104">Contenitore per uno o più elementi [PropertyDescription](./propdesc-schema-propertydescription.md) singoli.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-104">Container for one or many individual [propertyDescription](./propdesc-schema-propertydescription.md) elements.</span></span> <span data-ttu-id="b9e2a-105">Un file di schema della descrizione della proprietà. propdesc deve contenere almeno un elemento [propertyDescriptionList]() .</span><span class="sxs-lookup"><span data-stu-id="b9e2a-105">A .propdesc property description schema file should contain at least one [propertyDescriptionList]() element.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e2a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9e2a-106">Syntax</span></span>


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="b9e2a-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b9e2a-107">Element Information</span></span>



| <span data-ttu-id="b9e2a-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="b9e2a-108">Parent Element</span></span>                        | <span data-ttu-id="b9e2a-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b9e2a-109">Child Elements</span></span>                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="b9e2a-110">schema</span><span class="sxs-lookup"><span data-stu-id="b9e2a-110">schema</span></span>](./propdesc-schema-entry.md) | [<span data-ttu-id="b9e2a-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="b9e2a-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a><span data-ttu-id="b9e2a-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="b9e2a-112">Attributes</span></span>



| <span data-ttu-id="b9e2a-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="b9e2a-113">Attribute</span></span> | <span data-ttu-id="b9e2a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9e2a-114">Description</span></span>                                                               |
|-----------|---------------------------------------------------------------------------|
| <span data-ttu-id="b9e2a-115">publisher</span><span class="sxs-lookup"><span data-stu-id="b9e2a-115">publisher</span></span> | <span data-ttu-id="b9e2a-116">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-116">Public.</span></span> <span data-ttu-id="b9e2a-117">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-117">Required.</span></span> <span data-ttu-id="b9e2a-118">Nome visualizzato del server di pubblicazione che fornisce lo schema.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-118">The display name of the publisher providing the schema.</span></span> |
| <span data-ttu-id="b9e2a-119">product</span><span class="sxs-lookup"><span data-stu-id="b9e2a-119">product</span></span>   | <span data-ttu-id="b9e2a-120">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-120">Public.</span></span> <span data-ttu-id="b9e2a-121">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-121">Required.</span></span> <span data-ttu-id="b9e2a-122">Nome visualizzato del prodotto che fornisce lo schema.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-122">The display name of the product providing the schema.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="b9e2a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9e2a-123">Remarks</span></span>

<span data-ttu-id="b9e2a-124">Il [propertyDescriptionList]() non deve essere confuso con "elenchi di proprietà" e [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), che sono completamente distinti.</span><span class="sxs-lookup"><span data-stu-id="b9e2a-124">The [propertyDescriptionList]() should not be confused with "property lists" and [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which are completely separate.</span></span>

 

 
