---
description: 'Specifica il modo in cui IPropertyDescription:: FormatForDisplay deve formattare il valore della proprietà come stringa. Questa operazione è applicabile solo se <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91332f0cc062e7ee4a83e3584776ecf09c5c4b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967585"
---
# <a name="booleanformat"></a><span data-ttu-id="f3c35-104">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="f3c35-104">booleanFormat</span></span>

<span data-ttu-id="f3c35-105">Specifica il modo in cui [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formattare il valore della proprietà come stringa.</span><span class="sxs-lookup"><span data-stu-id="f3c35-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="f3c35-106">Questa operazione è applicabile solo se <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="f3c35-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="f3c35-107">Deve essere presente un solo elemento [booleanFormat]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c35-107">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="f3c35-108">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="f3c35-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="f3c35-109">Se non viene specificato alcun elemento [booleanFormat]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f3c35-109">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3c35-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3c35-110">Syntax</span></span>


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="YesNo"/>
                <xs:enumeration value="OnOff"/>
                <xs:enumeration value="TrueFalse"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="f3c35-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f3c35-111">Element Information</span></span>



| <span data-ttu-id="f3c35-112">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="f3c35-112">Parent Element</span></span>                                   | <span data-ttu-id="f3c35-113">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f3c35-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="f3c35-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f3c35-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="f3c35-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="f3c35-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="f3c35-116">Attributi</span><span class="sxs-lookup"><span data-stu-id="f3c35-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3c35-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="f3c35-117">Attribute</span></span></th>
<th><span data-ttu-id="f3c35-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3c35-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3c35-119">formato</span><span class="sxs-lookup"><span data-stu-id="f3c35-119">formatAs</span></span></td>
<td><span data-ttu-id="f3c35-120">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="f3c35-120">Public.</span></span> <span data-ttu-id="f3c35-121">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f3c35-121">Optional.</span></span> <span data-ttu-id="f3c35-122">Il valore predefinito è &quot; YesNo &quot; .</span><span class="sxs-lookup"><span data-stu-id="f3c35-122">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="f3c35-123">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3c35-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f3c35-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f3c35-124">Value</span></span></th>
<th><span data-ttu-id="f3c35-125">Significato</span><span class="sxs-lookup"><span data-stu-id="f3c35-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3c35-126">YesNo</span><span class="sxs-lookup"><span data-stu-id="f3c35-126">YesNo</span></span></td>
<td><span data-ttu-id="f3c35-127">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f3c35-127">Default.</span></span> <span data-ttu-id="f3c35-128">Formatta il valore come &quot; Yes &quot; o &quot; No &quot; .</span><span class="sxs-lookup"><span data-stu-id="f3c35-128">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="f3c35-129">Richiede che il tipo di proprietà sia booleano.</span><span class="sxs-lookup"><span data-stu-id="f3c35-129">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c35-130">OnOff</span><span class="sxs-lookup"><span data-stu-id="f3c35-130">OnOff</span></span></td>
<td><span data-ttu-id="f3c35-131">Formatta il valore come &quot; on &quot; o &quot; off &quot; .</span><span class="sxs-lookup"><span data-stu-id="f3c35-131">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="f3c35-132">Richiede che il tipo di proprietà sia booleano.</span><span class="sxs-lookup"><span data-stu-id="f3c35-132">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3c35-133">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="f3c35-133">TrueFalse</span></span></td>
<td><span data-ttu-id="f3c35-134">Formatta il valore come &quot; true &quot; o &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="f3c35-134">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="f3c35-135">Richiede che il tipo di proprietà sia booleano.</span><span class="sxs-lookup"><span data-stu-id="f3c35-135">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
