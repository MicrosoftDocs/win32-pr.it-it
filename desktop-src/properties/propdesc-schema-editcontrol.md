---
description: Specifica il controllo da utilizzare durante la modifica della proprietà.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967584"
---
# <a name="editcontrol"></a><span data-ttu-id="e823e-103">editControl</span><span class="sxs-lookup"><span data-stu-id="e823e-103">editControl</span></span>

<span data-ttu-id="e823e-104">Specifica il controllo da utilizzare durante la modifica della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e823e-104">Specifies what control to use when editing the property.</span></span> <span data-ttu-id="e823e-105">Deve essere presente un solo elemento [editControl]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e823e-105">There should be only one [editControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="e823e-106">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="e823e-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="e823e-107">Se non viene specificato alcun elemento [editControl]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e823e-107">If no [editControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="e823e-108">Se <typeInfo isInnate="true"> , questo elemento viene ignorato perché non è possibile modificare una proprietà innata.</span><span class="sxs-lookup"><span data-stu-id="e823e-108">If <typeInfo isInnate="true">, this element is ignored because an innate property cannot be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="e823e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e823e-109">Syntax</span></span>


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="e823e-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e823e-110">Element Information</span></span>



| <span data-ttu-id="e823e-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e823e-111">Parent Element</span></span>                                   | <span data-ttu-id="e823e-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e823e-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="e823e-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e823e-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="e823e-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="e823e-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="e823e-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="e823e-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e823e-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="e823e-116">Attribute</span></span></th>
<th><span data-ttu-id="e823e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e823e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e823e-118">controllo</span><span class="sxs-lookup"><span data-stu-id="e823e-118">control</span></span></td>
<td><span data-ttu-id="e823e-119">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="e823e-119">Public.</span></span> <span data-ttu-id="e823e-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e823e-120">Optional.</span></span> <span data-ttu-id="e823e-121">Il valore predefinito è &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="e823e-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="e823e-122">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="e823e-122">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e823e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e823e-123">Value</span></span></th>
<th><span data-ttu-id="e823e-124">Significato</span><span class="sxs-lookup"><span data-stu-id="e823e-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e823e-125">Predefinito</span><span class="sxs-lookup"><span data-stu-id="e823e-125">Default</span></span></td>
<td><span data-ttu-id="e823e-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e823e-126">Default.</span></span> <span data-ttu-id="e823e-127">Usa il controllo predefinito, in base all' <typeInfo type=&quot;&quot;> attributo.</span><span class="sxs-lookup"><span data-stu-id="e823e-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="e823e-128">I tipi predefiniti sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="e823e-128">The default types are listed below.</span></span> <span data-ttu-id="e823e-129">Qualsiasi altro tipo comporta l'utilizzo del &quot; controllo di testo &quot; .</span><span class="sxs-lookup"><span data-stu-id="e823e-129">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e823e-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="e823e-130">Type</span></span></th>
<th><span data-ttu-id="e823e-131">Control</span><span class="sxs-lookup"><span data-stu-id="e823e-131">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e823e-132">string</span><span class="sxs-lookup"><span data-stu-id="e823e-132">String</span></span></td>
<td><span data-ttu-id="e823e-133">Testo</span><span class="sxs-lookup"><span data-stu-id="e823e-133">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e823e-134">String (multivalore)</span><span class="sxs-lookup"><span data-stu-id="e823e-134">String (multi-value)</span></span></td>
<td><span data-ttu-id="e823e-135">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="e823e-135">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e823e-136">Datetime</span><span class="sxs-lookup"><span data-stu-id="e823e-136">DateTime</span></span></td>
<td><span data-ttu-id="e823e-137">Calendario</span><span class="sxs-lookup"><span data-stu-id="e823e-137">Calendar</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e823e-138">Calendario</span><span class="sxs-lookup"><span data-stu-id="e823e-138">Calendar</span></span></td>
<td><span data-ttu-id="e823e-139">Usa il controllo Calendar.</span><span class="sxs-lookup"><span data-stu-id="e823e-139">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e823e-140">CheckboxDropList</span><span class="sxs-lookup"><span data-stu-id="e823e-140">CheckboxDropList</span></span></td>
<td><span data-ttu-id="e823e-141">Usa il controllo elenco con le caselle di controllo.</span><span class="sxs-lookup"><span data-stu-id="e823e-141">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e823e-142">DropList</span><span class="sxs-lookup"><span data-stu-id="e823e-142">DropList</span></span></td>
<td><span data-ttu-id="e823e-143">Usa il controllo elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="e823e-143">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e823e-144">MultiLineText</span><span class="sxs-lookup"><span data-stu-id="e823e-144">MultiLineText</span></span></td>
<td><span data-ttu-id="e823e-145">Utilizza il controllo di modifica del testo su più righe.</span><span class="sxs-lookup"><span data-stu-id="e823e-145">Uses the multi-line text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e823e-146">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="e823e-146">MultiValueText</span></span></td>
<td><span data-ttu-id="e823e-147">Utilizza il controllo di modifica del testo multivalore.</span><span class="sxs-lookup"><span data-stu-id="e823e-147">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e823e-148">Classificazione</span><span class="sxs-lookup"><span data-stu-id="e823e-148">Rating</span></span></td>
<td><span data-ttu-id="e823e-149">Usa il controllo della classificazione a 5 stelle.</span><span class="sxs-lookup"><span data-stu-id="e823e-149">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e823e-150">Testo</span><span class="sxs-lookup"><span data-stu-id="e823e-150">Text</span></span></td>
<td><span data-ttu-id="e823e-151">Utilizza il controllo di modifica del testo.</span><span class="sxs-lookup"><span data-stu-id="e823e-151">Uses the text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e823e-152">IconList</span><span class="sxs-lookup"><span data-stu-id="e823e-152">IconList</span></span></td>
<td><span data-ttu-id="e823e-153"><strong>Windows 7 e versioni successive.</strong></span><span class="sxs-lookup"><span data-stu-id="e823e-153"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
