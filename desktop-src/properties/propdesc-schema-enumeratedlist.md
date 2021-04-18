---
description: 'Specifica il modo in cui IPropertyDescription:: FormatForDisplay deve formattare il valore della proprietà come stringa.'
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: enumeratedList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312550"
---
# <a name="enumeratedlist"></a><span data-ttu-id="0e4c1-103">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="0e4c1-103">enumeratedList</span></span>

<span data-ttu-id="0e4c1-104">Specifica il modo in cui [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formattare il valore della proprietà come stringa.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="0e4c1-105">Influenza inoltre il modo in cui la proprietà può essere raggruppata o i valori da visualizzare nell'elenco se "editControl" è un listblox.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-105">It also influences how the property may be grouped, or what values to show in the list if the "editControl" is a listblox.</span></span> <span data-ttu-id="0e4c1-106">Questa operazione è applicabile solo se <displayInfo displayType="Enumerated"> .</span><span class="sxs-lookup"><span data-stu-id="0e4c1-106">This is applicable only if <displayInfo displayType="Enumerated">.</span></span> <span data-ttu-id="0e4c1-107">Deve essere presente un solo elemento [enumeratedList]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="0e4c1-107">There should be only one [enumeratedList]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="0e4c1-108">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="0e4c1-109">Se non viene specificato alcun elemento [enumeratedList]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-109">If no [enumeratedList]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e4c1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e4c1-110">Syntax</span></span>


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="0e4c1-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0e4c1-111">Element Information</span></span>



| <span data-ttu-id="0e4c1-112">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="0e4c1-112">Parent Element</span></span>                                   | <span data-ttu-id="0e4c1-113">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0e4c1-113">Child Elements</span></span>                               |
|--------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="0e4c1-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0e4c1-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | [<span data-ttu-id="0e4c1-115">enum</span><span class="sxs-lookup"><span data-stu-id="0e4c1-115">enum</span></span>](./propdesc-schema-enum.md)           |
|                                                  | [<span data-ttu-id="0e4c1-116">enumRange</span><span class="sxs-lookup"><span data-stu-id="0e4c1-116">enumRange</span></span>](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a><span data-ttu-id="0e4c1-117">Attributi</span><span class="sxs-lookup"><span data-stu-id="0e4c1-117">Attributes</span></span>



| <span data-ttu-id="0e4c1-118">Attributo</span><span class="sxs-lookup"><span data-stu-id="0e4c1-118">Attribute</span></span>          | <span data-ttu-id="0e4c1-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e4c1-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e4c1-120">defaultText</span><span class="sxs-lookup"><span data-stu-id="0e4c1-120">defaultText</span></span>        | <span data-ttu-id="0e4c1-121">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-121">Public.</span></span> <span data-ttu-id="0e4c1-122">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-122">Optional.</span></span> <span data-ttu-id="0e4c1-123">Specificare il testo predefinito da usare se viene assegnato un valore a [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) che non esegue il mapping a uno degli elementi enumerati nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-123">Specify default text to use if a value is given to [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) that does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="0e4c1-124">La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto a una stringa di visualizzazione. usare il riferimento, in modo che possa essere localizzato.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-124">The syntax allows for a direct display string or an indirect display string reference; use the reference, so it can be localized.</span></span>                              |
| <span data-ttu-id="0e4c1-125">useValueForDefault</span><span class="sxs-lookup"><span data-stu-id="0e4c1-125">useValueForDefault</span></span> | <span data-ttu-id="0e4c1-126">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-126">Public.</span></span> <span data-ttu-id="0e4c1-127">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-127">Optional.</span></span> <span data-ttu-id="0e4c1-128">Se si imposta questa opzione su "true", [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) utilizzerà il valore così com'è, se il valore non viene mappato a uno degli elementi enumerati nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-128">Setting this to "true" will inform [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) to use the value as-is if the value does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="0e4c1-129">Per **IPropertyDescription:: FormatForDisplay**, impostando questo valore su "true" si ha la precedenza sull'impostazione di "DefaultText".</span><span class="sxs-lookup"><span data-stu-id="0e4c1-129">For **IPropertyDescription::FormatForDisplay**, setting this to "true" takes precedence over setting the "defaultText".</span></span> <span data-ttu-id="0e4c1-130">Il valore predefinito è "false".</span><span class="sxs-lookup"><span data-stu-id="0e4c1-130">The default is "false".</span></span> |



 

 

 
