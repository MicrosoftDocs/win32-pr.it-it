---
description: Specifica il modo in cui IPropertyDescription::FormatForDisplay deve formattare il valore della proprietà booleanFormat come stringa.
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 528458d9c31d54ef43eca8325b1daeef4eee1195
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405964"
---
# <a name="booleanformat"></a><span data-ttu-id="22f97-103">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="22f97-103">booleanFormat</span></span>

<span data-ttu-id="22f97-104">Specifica il modo [**in cui IPropertyDescription::FormatForDisplay deve**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) formattare il valore della proprietà come stringa.</span><span class="sxs-lookup"><span data-stu-id="22f97-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="22f97-105">Questa opzione è applicabile solo se <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="22f97-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="22f97-106">Deve essere presente un solo [elemento booleanFormat]() per ogni [elemento displayInfo.](./propdesc-schema-displayinfo.md)</span><span class="sxs-lookup"><span data-stu-id="22f97-106">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="22f97-107">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="22f97-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="22f97-108">Se non [viene specificato alcun elemento booleanFormat,]() le impostazioni predefinite dell'attributo vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="22f97-108">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="22f97-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22f97-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="22f97-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="22f97-110">Element Information</span></span>



| <span data-ttu-id="22f97-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="22f97-111">Parent Element</span></span>                                   | <span data-ttu-id="22f97-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="22f97-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="22f97-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="22f97-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="22f97-114">Nessuno</span><span class="sxs-lookup"><span data-stu-id="22f97-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="22f97-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="22f97-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22f97-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="22f97-116">Attribute</span></span></th>
<th><span data-ttu-id="22f97-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22f97-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22f97-118">formatAs</span><span class="sxs-lookup"><span data-stu-id="22f97-118">formatAs</span></span></td>
<td><span data-ttu-id="22f97-119">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="22f97-119">Public.</span></span> <span data-ttu-id="22f97-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="22f97-120">Optional.</span></span> <span data-ttu-id="22f97-121">Il valore predefinito &quot; è YesNo &quot; .</span><span class="sxs-lookup"><span data-stu-id="22f97-121">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="22f97-122">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="22f97-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="22f97-123">Valore</span><span class="sxs-lookup"><span data-stu-id="22f97-123">Value</span></span></th>
<th><span data-ttu-id="22f97-124">Significato</span><span class="sxs-lookup"><span data-stu-id="22f97-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22f97-125">YesNo</span><span class="sxs-lookup"><span data-stu-id="22f97-125">YesNo</span></span></td>
<td><span data-ttu-id="22f97-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="22f97-126">Default.</span></span> <span data-ttu-id="22f97-127">Formatta il valore come &quot; Sì &quot; o &quot; &quot; No.</span><span class="sxs-lookup"><span data-stu-id="22f97-127">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="22f97-128">Richiede che il tipo di proprietà sia booleano.</span><span class="sxs-lookup"><span data-stu-id="22f97-128">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22f97-129">Onoff</span><span class="sxs-lookup"><span data-stu-id="22f97-129">OnOff</span></span></td>
<td><span data-ttu-id="22f97-130">Formatta il valore come &quot; On &quot; o &quot; &quot; Off.</span><span class="sxs-lookup"><span data-stu-id="22f97-130">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="22f97-131">Richiede che il tipo di proprietà sia booleano.</span><span class="sxs-lookup"><span data-stu-id="22f97-131">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22f97-132">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="22f97-132">TrueFalse</span></span></td>
<td><span data-ttu-id="22f97-133">Formatta il valore come &quot; True &quot; o &quot; &quot; False.</span><span class="sxs-lookup"><span data-stu-id="22f97-133">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="22f97-134">Richiede che il tipo di proprietà sia booleano.</span><span class="sxs-lookup"><span data-stu-id="22f97-134">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
