---
description: Specifica il controllo da utilizzare quando si visualizza semplicemente la proprietà.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: drawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049788"
---
# <a name="drawcontrol"></a><span data-ttu-id="e4c63-103">drawControl</span><span class="sxs-lookup"><span data-stu-id="e4c63-103">drawControl</span></span>

<span data-ttu-id="e4c63-104">Specifica il controllo da utilizzare quando si visualizza semplicemente la proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4c63-104">Specifies what control to use when simply displaying the property.</span></span> <span data-ttu-id="e4c63-105">Deve essere presente un solo elemento [drawControl]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e4c63-105">There should be only one [drawControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="e4c63-106">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="e4c63-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="e4c63-107">Se non viene specificato alcun elemento [drawControl]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4c63-107">If no [drawControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="e4c63-108">Questo formato del controllo non consente la modifica delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4c63-108">This form of the control does not allow for property editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c63-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4c63-109">Syntax</span></span>


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="e4c63-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e4c63-110">Element Information</span></span>



| <span data-ttu-id="e4c63-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e4c63-111">Parent Element</span></span>                                   | <span data-ttu-id="e4c63-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e4c63-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="e4c63-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e4c63-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="e4c63-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="e4c63-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="e4c63-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="e4c63-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e4c63-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="e4c63-116">Attribute</span></span></th>
<th><span data-ttu-id="e4c63-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4c63-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4c63-118">controllo</span><span class="sxs-lookup"><span data-stu-id="e4c63-118">control</span></span></td>
<td><span data-ttu-id="e4c63-119">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="e4c63-119">Public.</span></span> <span data-ttu-id="e4c63-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e4c63-120">Optional.</span></span> <span data-ttu-id="e4c63-121">Il valore predefinito è &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="e4c63-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="e4c63-122">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="e4c63-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e4c63-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e4c63-123">Value</span></span></th>
<th><span data-ttu-id="e4c63-124">Significato</span><span class="sxs-lookup"><span data-stu-id="e4c63-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4c63-125">Predefinito</span><span class="sxs-lookup"><span data-stu-id="e4c63-125">Default</span></span></td>
<td><span data-ttu-id="e4c63-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e4c63-126">Default.</span></span> <span data-ttu-id="e4c63-127">Usa il controllo predefinito, in base all' <typeInfo type=&quot;&quot;> attributo.</span><span class="sxs-lookup"><span data-stu-id="e4c63-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="e4c63-128">Il tipo predefinito è &quot; String &quot; (multivalore) e il controllo predefinito è &quot; MultiValueText &quot; .</span><span class="sxs-lookup"><span data-stu-id="e4c63-128">The default type is &quot;String&quot; (multi-value) and the default control is &quot;MultiValueText&quot;.</span></span> <span data-ttu-id="e4c63-129">Qualsiasi altro tipo comporta l'uso del &quot; &quot; controllo StaticText.</span><span class="sxs-lookup"><span data-stu-id="e4c63-129">Any other type results in using the &quot;StaticText&quot; control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4c63-130">MultiLineText</span><span class="sxs-lookup"><span data-stu-id="e4c63-130">MultiLineText</span></span></td>
<td><span data-ttu-id="e4c63-131">Usa il controllo testo a più righe.</span><span class="sxs-lookup"><span data-stu-id="e4c63-131">Uses the multi-line text control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4c63-132">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="e4c63-132">MultiValueText</span></span></td>
<td><span data-ttu-id="e4c63-133">Usa il controllo di testo multivalore.</span><span class="sxs-lookup"><span data-stu-id="e4c63-133">Uses the multi-value text control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4c63-134">PercentBar</span><span class="sxs-lookup"><span data-stu-id="e4c63-134">PercentBar</span></span></td>
<td><span data-ttu-id="e4c63-135">Usa il controllo barra percentuale.</span><span class="sxs-lookup"><span data-stu-id="e4c63-135">Uses the percent bar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4c63-136">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="e4c63-136">ProgressBar</span></span></td>
<td><span data-ttu-id="e4c63-137">Usa il controllo indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="e4c63-137">Uses the progress bar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4c63-138">Classificazione</span><span class="sxs-lookup"><span data-stu-id="e4c63-138">Rating</span></span></td>
<td><span data-ttu-id="e4c63-139">Usa il controllo della classificazione a 5 stelle.</span><span class="sxs-lookup"><span data-stu-id="e4c63-139">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4c63-140">StaticText</span><span class="sxs-lookup"><span data-stu-id="e4c63-140">StaticText</span></span></td>
<td><span data-ttu-id="e4c63-141">USA <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription:: FormatForDisplay</strong></a> per visualizzare il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4c63-141">Uses <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription::FormatForDisplay</strong></a> to display the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4c63-142">IconList</span><span class="sxs-lookup"><span data-stu-id="e4c63-142">IconList</span></span></td>
<td><span data-ttu-id="e4c63-143"><strong>Windows 7 e versioni successive.</strong></span><span class="sxs-lookup"><span data-stu-id="e4c63-143"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="e4c63-144">Enumerazione di icone.</span><span class="sxs-lookup"><span data-stu-id="e4c63-144">An enumeration of icons.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4c63-145">BooleanCheckMark</span><span class="sxs-lookup"><span data-stu-id="e4c63-145">BooleanCheckMark</span></span></td>
<td><span data-ttu-id="e4c63-146"><strong>Windows 7 e versioni successive.</strong></span><span class="sxs-lookup"><span data-stu-id="e4c63-146"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
