---
description: Descrive una singola proprietà canonica univoca.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: propertyDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967109"
---
# <a name="propertydescription"></a><span data-ttu-id="30678-103">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="30678-103">propertyDescription</span></span>

<span data-ttu-id="30678-104">Descrive una singola proprietà canonica univoca.</span><span class="sxs-lookup"><span data-stu-id="30678-104">Describes a single unique canonical property.</span></span> <span data-ttu-id="30678-105">Ogni proprietà di questo tipo destinata a essere disponibile nel sistema deve avere un elemento [PropertyDescription]() corrispondente.</span><span class="sxs-lookup"><span data-stu-id="30678-105">Every such property intended to be available in the system must have a corresponding [propertyDescription]() element.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="30678-106">Sintassi per Windows 7</span><span class="sxs-lookup"><span data-stu-id="30678-106">Syntax for Windows 7</span></span>


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a><span data-ttu-id="30678-107">Sintassi per vista</span><span class="sxs-lookup"><span data-stu-id="30678-107">Syntax for Vista</span></span>


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="30678-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="30678-108">Element Information</span></span>



| <span data-ttu-id="30678-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="30678-109">Parent Element</span></span>                                                           | <span data-ttu-id="30678-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="30678-110">Child Elements</span></span>                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="30678-111">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="30678-111">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md) | [<span data-ttu-id="30678-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="30678-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [<span data-ttu-id="30678-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="30678-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [<span data-ttu-id="30678-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="30678-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [<span data-ttu-id="30678-115">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="30678-115">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [<span data-ttu-id="30678-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="30678-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [<span data-ttu-id="30678-117">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="30678-117">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a><span data-ttu-id="30678-118">Attributi</span><span class="sxs-lookup"><span data-stu-id="30678-118">Attributes</span></span>



| <span data-ttu-id="30678-119">Attributo</span><span class="sxs-lookup"><span data-stu-id="30678-119">Attribute</span></span> | <span data-ttu-id="30678-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30678-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30678-121">name</span><span class="sxs-lookup"><span data-stu-id="30678-121">name</span></span>      | <span data-ttu-id="30678-122">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="30678-122">Required.</span></span> <span data-ttu-id="30678-123">Nome di proprietà canonico, univoco per il sistema; ad esempio, `System.Rating` .</span><span class="sxs-lookup"><span data-stu-id="30678-123">The canonical property name, unique to the system; for example, `System.Rating`.</span></span> <span data-ttu-id="30678-124">La stringa è di tipo canonico ed è limitata a 64 caratteri.</span><span class="sxs-lookup"><span data-stu-id="30678-124">This string is of type canonical-type and is limited to 64 characters.</span></span> <span data-ttu-id="30678-125">Il nome fa distinzione tra maiuscole e minuscole e deve usare la sintassi seguente: Publisher. Application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="30678-125">The name is case-sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="30678-126">[**IPropertyDescription:: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) restituisce questo valore.</span><span class="sxs-lookup"><span data-stu-id="30678-126">[**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) returns this value.</span></span> |
| <span data-ttu-id="30678-127">formatID</span><span class="sxs-lookup"><span data-stu-id="30678-127">formatID</span></span>  | <span data-ttu-id="30678-128">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="30678-128">Required.</span></span> <span data-ttu-id="30678-129">Identificatore di formato della proprietà (FMTID).</span><span class="sxs-lookup"><span data-stu-id="30678-129">The property's format identifier (FMTID).</span></span> <span data-ttu-id="30678-130">Il valore deve includere le parentesi graffe di inclusione. ad esempio, `{64440492-4C8B-11D1-8B70-080036B11A03}` .</span><span class="sxs-lookup"><span data-stu-id="30678-130">The value must include enclosing braces; for example, `{64440492-4C8B-11D1-8B70-080036B11A03}`.</span></span> <span data-ttu-id="30678-131">[**IPropertyDescription:: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) restituisce questo valore.</span><span class="sxs-lookup"><span data-stu-id="30678-131">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span>                                                                                                                       |
| <span data-ttu-id="30678-132">propID</span><span class="sxs-lookup"><span data-stu-id="30678-132">propID</span></span>    | <span data-ttu-id="30678-133">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="30678-133">Required.</span></span> <span data-ttu-id="30678-134">Identificatore di proprietà (PID); ad esempio, `9` .</span><span class="sxs-lookup"><span data-stu-id="30678-134">The property identifier (PID); for example, `9`.</span></span> <span data-ttu-id="30678-135">[**IPropertyDescription:: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) restituisce questo valore.</span><span class="sxs-lookup"><span data-stu-id="30678-135">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span> <span data-ttu-id="30678-136">Questo valore deve essere maggiore o uguale a 2.</span><span class="sxs-lookup"><span data-stu-id="30678-136">This value must be greater than or equal to 2.</span></span> <span data-ttu-id="30678-137">I valori 0 e 1 sono riservati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="30678-137">The values 0 and 1 are reserved by the system.</span></span>                                                                                                                  |



 

 

 
