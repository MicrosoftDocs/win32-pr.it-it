---
description: Non supportato in Windows 7 e versioni successive. Specifica il controllo da utilizzare nel generatore di query.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448b47038f82afb9f860209bfe89eb9e6eecb890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310115"
---
# <a name="querycontrol"></a><span data-ttu-id="f5d91-104">queryControl</span><span class="sxs-lookup"><span data-stu-id="f5d91-104">queryControl</span></span>

<span data-ttu-id="f5d91-105">Non supportato in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f5d91-105">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="f5d91-106">Specifica il controllo da utilizzare nel generatore di query.</span><span class="sxs-lookup"><span data-stu-id="f5d91-106">Specifies what control to use in the query builder.</span></span> <span data-ttu-id="f5d91-107">Deve essere presente un solo elemento [queryControl]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="f5d91-107">There should be only one [queryControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="f5d91-108">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="f5d91-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="f5d91-109">Se non viene specificato alcun elemento [queryControl]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f5d91-109">If no [queryControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d91-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5d91-110">Syntax</span></span>


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="f5d91-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f5d91-111">Element Information</span></span>



| <span data-ttu-id="f5d91-112">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="f5d91-112">Parent Element</span></span>                                   | <span data-ttu-id="f5d91-113">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f5d91-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="f5d91-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f5d91-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="f5d91-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="f5d91-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="f5d91-116">Attributi</span><span class="sxs-lookup"><span data-stu-id="f5d91-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f5d91-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="f5d91-117">Attribute</span></span></th>
<th><span data-ttu-id="f5d91-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5d91-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f5d91-119">controllo</span><span class="sxs-lookup"><span data-stu-id="f5d91-119">control</span></span></td>
<td><span data-ttu-id="f5d91-120">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="f5d91-120">Public.</span></span> <span data-ttu-id="f5d91-121">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f5d91-121">Optional.</span></span> <span data-ttu-id="f5d91-122">Il valore predefinito è &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="f5d91-122">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="f5d91-123">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5d91-123">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f5d91-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f5d91-124">Value</span></span></th>
<th><span data-ttu-id="f5d91-125">Significato</span><span class="sxs-lookup"><span data-stu-id="f5d91-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f5d91-126">Predefinito</span><span class="sxs-lookup"><span data-stu-id="f5d91-126">Default</span></span></td>
<td><span data-ttu-id="f5d91-127">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f5d91-127">Default.</span></span> <span data-ttu-id="f5d91-128">Usa il controllo predefinito, in base all' <typeInfo type=&quot;&quot;> attributo.</span><span class="sxs-lookup"><span data-stu-id="f5d91-128">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="f5d91-129">I tipi predefiniti sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="f5d91-129">The default types are listed below.</span></span> <span data-ttu-id="f5d91-130">Qualsiasi altro tipo comporta l'utilizzo del &quot; controllo di testo &quot; .</span><span class="sxs-lookup"><span data-stu-id="f5d91-130">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f5d91-131">ConditionType</span><span class="sxs-lookup"><span data-stu-id="f5d91-131">ConditionType</span></span></th>
<th><span data-ttu-id="f5d91-132">Control</span><span class="sxs-lookup"><span data-stu-id="f5d91-132">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f5d91-133">string</span><span class="sxs-lookup"><span data-stu-id="f5d91-133">String</span></span></td>
<td><span data-ttu-id="f5d91-134">Testo</span><span class="sxs-lookup"><span data-stu-id="f5d91-134">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5d91-135">String (multivalore)</span><span class="sxs-lookup"><span data-stu-id="f5d91-135">String (multi-value)</span></span></td>
<td><span data-ttu-id="f5d91-136">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="f5d91-136">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5d91-137">Numero o dimensioni</span><span class="sxs-lookup"><span data-stu-id="f5d91-137">Number or Size</span></span></td>
<td><span data-ttu-id="f5d91-138">NumericText</span><span class="sxs-lookup"><span data-stu-id="f5d91-138">NumericText</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5d91-139">Numero o dimensione (enumerazione)</span><span class="sxs-lookup"><span data-stu-id="f5d91-139">Number or Size (enum)</span></span></td>
<td><span data-ttu-id="f5d91-140">Elenco</span><span class="sxs-lookup"><span data-stu-id="f5d91-140">List</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5d91-141">Datetime</span><span class="sxs-lookup"><span data-stu-id="f5d91-141">DateTime</span></span></td>
<td><span data-ttu-id="f5d91-142">Calendario</span><span class="sxs-lookup"><span data-stu-id="f5d91-142">Calendar</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5d91-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="f5d91-143">Boolean</span></span></td>
<td><span data-ttu-id="f5d91-144">Boolean</span><span class="sxs-lookup"><span data-stu-id="f5d91-144">Boolean</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5d91-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="f5d91-145">Boolean</span></span></td>
<td><span data-ttu-id="f5d91-146">Usa il controllo booleano.</span><span class="sxs-lookup"><span data-stu-id="f5d91-146">Uses the boolean control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5d91-147">Calendario</span><span class="sxs-lookup"><span data-stu-id="f5d91-147">Calendar</span></span></td>
<td><span data-ttu-id="f5d91-148">Usa il controllo del calendario a discesa.</span><span class="sxs-lookup"><span data-stu-id="f5d91-148">Uses the dropdown calendar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5d91-149">CheckboxDropList</span><span class="sxs-lookup"><span data-stu-id="f5d91-149">CheckboxDropList</span></span></td>
<td><span data-ttu-id="f5d91-150">Usa il controllo elenco con le caselle di controllo.</span><span class="sxs-lookup"><span data-stu-id="f5d91-150">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5d91-151">DropList</span><span class="sxs-lookup"><span data-stu-id="f5d91-151">DropList</span></span></td>
<td><span data-ttu-id="f5d91-152">Usa il controllo elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="f5d91-152">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5d91-153">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="f5d91-153">MultiValueText</span></span></td>
<td><span data-ttu-id="f5d91-154">Utilizza il controllo di modifica del testo multivalore.</span><span class="sxs-lookup"><span data-stu-id="f5d91-154">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5d91-155">NumericText</span><span class="sxs-lookup"><span data-stu-id="f5d91-155">NumericText</span></span></td>
<td><span data-ttu-id="f5d91-156">Utilizza il controllo di modifica del testo numerico.</span><span class="sxs-lookup"><span data-stu-id="f5d91-156">Uses the numeric text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5d91-157">Classificazione</span><span class="sxs-lookup"><span data-stu-id="f5d91-157">Rating</span></span></td>
<td><span data-ttu-id="f5d91-158">Usa il controllo della classificazione a 5 stelle.</span><span class="sxs-lookup"><span data-stu-id="f5d91-158">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5d91-159">Testo</span><span class="sxs-lookup"><span data-stu-id="f5d91-159">Text</span></span></td>
<td><span data-ttu-id="f5d91-160">Utilizza il controllo di modifica del testo.</span><span class="sxs-lookup"><span data-stu-id="f5d91-160">Uses the text edit control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
