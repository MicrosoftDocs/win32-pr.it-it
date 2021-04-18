---
description: Specifica la modalità di visualizzazione delle etichette della proprietà.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310121"
---
# <a name="labelinfo"></a><span data-ttu-id="67915-103">labelInfo</span><span class="sxs-lookup"><span data-stu-id="67915-103">labelInfo</span></span>

<span data-ttu-id="67915-104">Specifica la modalità di visualizzazione delle etichette della proprietà.</span><span class="sxs-lookup"><span data-stu-id="67915-104">Specifies how the property's labels are displayed.</span></span> <span data-ttu-id="67915-105">Deve essere presente un solo elemento [labelInfo]() per ogni elemento [PropertyDescription](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="67915-105">There should be only one [labelInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

<span data-ttu-id="67915-106">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="67915-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="67915-107">Se non viene specificato alcun elemento [labelInfo]() , l'etichetta della proprietà non viene visualizzata; Tuttavia, si tratta in genere di un difetto.</span><span class="sxs-lookup"><span data-stu-id="67915-107">If no [labelInfo]() element is provided, then the property's label is not displayed; however, this would typically be a defect.</span></span>

## <a name="syntax"></a><span data-ttu-id="67915-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67915-108">Syntax</span></span>


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="67915-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="67915-109">Element Information</span></span>



| <span data-ttu-id="67915-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="67915-110">Parent Element</span></span>                                                   | <span data-ttu-id="67915-111">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="67915-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="67915-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="67915-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="67915-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="67915-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="67915-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="67915-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67915-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="67915-115">Attribute</span></span></th>
<th><span data-ttu-id="67915-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67915-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67915-117">label</span><span class="sxs-lookup"><span data-stu-id="67915-117">label</span></span></td>
<td><span data-ttu-id="67915-118">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="67915-118">Public.</span></span> <span data-ttu-id="67915-119">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="67915-119">Optional.</span></span> <span data-ttu-id="67915-120">Etichetta visualizzata nell'interfaccia utente (ad esempio, l'etichetta della colonna dettagli o il riquadro di anteprima).</span><span class="sxs-lookup"><span data-stu-id="67915-120">The label as it is displayed in the UI (for example, the details column label or preview pane).</span></span> <span data-ttu-id="67915-121">La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto a una stringa di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="67915-121">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="67915-122">Utilizzare la stringa di visualizzazione indiretta perché può essere localizzata.</span><span class="sxs-lookup"><span data-stu-id="67915-122">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="67915-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription:: GetDisplayName</strong></a> restituisce il nome visualizzato risolto.</span><span class="sxs-lookup"><span data-stu-id="67915-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription::GetDisplayName</strong></a> returns the resolved display name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67915-124">sortDescription</span><span class="sxs-lookup"><span data-stu-id="67915-124">sortDescription</span></span></td>
<td><span data-ttu-id="67915-125">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="67915-125">Optional.</span></span> <span data-ttu-id="67915-126">Specifica le stringhe offerte come opzioni di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="67915-126">Specifies the strings offered as sort options.</span></span> <span data-ttu-id="67915-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription:: GetSortDescription</strong></a> restituisce questa descrizione di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="67915-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription::GetSortDescription</strong></a> returns this sort description.</span></span> <span data-ttu-id="67915-128">I valori seguenti forniscono le stringhe dell'interfaccia utente corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="67915-128">The following values provide the corresponding UI strings.</span></span>
<ul>
<li><span data-ttu-id="67915-129">Generale: ordinamento in corso di ordinamento &quot; &quot;  /  &quot; in corso&quot;</span><span class="sxs-lookup"><span data-stu-id="67915-129">General: &quot;Sort going up&quot; / &quot;Sort going down&quot;</span></span></li>
<li><span data-ttu-id="67915-130">AToZ: &quot; a all'inizio &quot;  /  &quot; Z all'inizio&quot;</span><span class="sxs-lookup"><span data-stu-id="67915-130">AToZ: &quot;A on top&quot; / &quot;Z on top&quot;</span></span></li>
<li><span data-ttu-id="67915-131">LowestHighest: &quot; più basso nella parte superiore &quot;  /  &quot; più in alto nella parte superiore&quot;</span><span class="sxs-lookup"><span data-stu-id="67915-131">LowestHighest: &quot;Lowest on top&quot; / &quot;Highest on top&quot;</span></span></li>
<li><span data-ttu-id="67915-132">OldestNewest: il &quot; più recente all'inizio più &quot;  /  &quot; recente all'inizio&quot;</span><span class="sxs-lookup"><span data-stu-id="67915-132">OldestNewest: &quot;Oldest on top&quot; / &quot;Newest on top&quot;</span></span></li>
<li><span data-ttu-id="67915-133">SmallestLargest: più &quot; piccolo nella parte superiore &quot;  /  &quot; più grande all'inizio&quot;</span><span class="sxs-lookup"><span data-stu-id="67915-133">SmallestLargest: &quot;Smallest on top&quot; / &quot;Largest on top&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67915-134">invitationText</span><span class="sxs-lookup"><span data-stu-id="67915-134">invitationText</span></span></td>
<td><span data-ttu-id="67915-135">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="67915-135">Optional.</span></span> <span data-ttu-id="67915-136">Testo della stringa della Guida visualizzato come istruzioni per l'utente per il controllo o la descrizione comando (ad esempio, &quot; immettere il nome dell'autore &quot; ).</span><span class="sxs-lookup"><span data-stu-id="67915-136">The Help string text that is displayed as an instruction to the user for the control or ToolTip (for instance, &quot;Enter author name.&quot;).</span></span> <span data-ttu-id="67915-137">La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto a una stringa di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="67915-137">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="67915-138">Utilizzare la stringa di visualizzazione indiretta perché può essere localizzata.</span><span class="sxs-lookup"><span data-stu-id="67915-138">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="67915-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription:: GetEditInvitation</strong></a> restituisce il testo dell'invito risolto.</span><span class="sxs-lookup"><span data-stu-id="67915-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription::GetEditInvitation</strong></a> returns the resolved invitation text.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67915-140">hideLabel</span><span class="sxs-lookup"><span data-stu-id="67915-140">hideLabel</span></span></td>
<td><span data-ttu-id="67915-141">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="67915-141">Optional.</span></span> <span data-ttu-id="67915-142">Il valore predefinito è &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="67915-142">The default is &quot;false&quot;.</span></span> <span data-ttu-id="67915-143">Indica se l'etichetta è nascosta.</span><span class="sxs-lookup"><span data-stu-id="67915-143">Indicates whether the label is hidden.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
