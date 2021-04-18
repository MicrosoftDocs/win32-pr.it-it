---
description: 'Specifica il modo in cui IPropertyDescription:: FormatForDisplay deve formattare il valore della proprietà come stringa. Questa operazione è applicabile solo se <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec05a6eedf1734c1d62c0503027810ad05916160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310110"
---
# <a name="stringformat"></a><span data-ttu-id="90fdc-104">stringFormat</span><span class="sxs-lookup"><span data-stu-id="90fdc-104">stringFormat</span></span>

<span data-ttu-id="90fdc-105">Specifica il modo in cui [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formattare il valore della proprietà come stringa.</span><span class="sxs-lookup"><span data-stu-id="90fdc-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="90fdc-106">Questa operazione è applicabile solo se <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="90fdc-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="90fdc-107">Deve essere presente un solo elemento [StringFormat]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="90fdc-107">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="90fdc-108">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="90fdc-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="90fdc-109">Se non viene specificato alcun elemento [StringFormat]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="90fdc-109">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="90fdc-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90fdc-110">Syntax</span></span>


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="formatAs">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="FileName"/>
                    <xs:enumeration value="FilePath"/>
                    <xs:enumeration value="Hyperlink"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="90fdc-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="90fdc-111">Element Information</span></span>



| <span data-ttu-id="90fdc-112">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="90fdc-112">Parent Element</span></span>                                   | <span data-ttu-id="90fdc-113">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="90fdc-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="90fdc-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="90fdc-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="90fdc-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="90fdc-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="90fdc-116">Attributi</span><span class="sxs-lookup"><span data-stu-id="90fdc-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90fdc-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="90fdc-117">Attribute</span></span></th>
<th><span data-ttu-id="90fdc-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90fdc-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90fdc-119">formato</span><span class="sxs-lookup"><span data-stu-id="90fdc-119">formatAs</span></span></td>
<td><span data-ttu-id="90fdc-120">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="90fdc-120">Public.</span></span> <span data-ttu-id="90fdc-121">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="90fdc-121">Optional.</span></span> <span data-ttu-id="90fdc-122">Il valore predefinito è &quot; Generale &quot; .</span><span class="sxs-lookup"><span data-stu-id="90fdc-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="90fdc-123">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="90fdc-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="90fdc-124">Valore</span><span class="sxs-lookup"><span data-stu-id="90fdc-124">Value</span></span></th>
<th><span data-ttu-id="90fdc-125">Significato</span><span class="sxs-lookup"><span data-stu-id="90fdc-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90fdc-126">Generale</span><span class="sxs-lookup"><span data-stu-id="90fdc-126">General</span></span></td>
<td><span data-ttu-id="90fdc-127">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="90fdc-127">Default.</span></span> <span data-ttu-id="90fdc-128">Restituisce il valore come stringa non formattata.</span><span class="sxs-lookup"><span data-stu-id="90fdc-128">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90fdc-129">FileName</span><span class="sxs-lookup"><span data-stu-id="90fdc-129">FileName</span></span></td>
<td><span data-ttu-id="90fdc-130">Formatta il valore come nome file.</span><span class="sxs-lookup"><span data-stu-id="90fdc-130">Formats the value as a file name.</span></span> <span data-ttu-id="90fdc-131">Nasconde l'estensione in base alle impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="90fdc-131">Hides the extension according to user settings.</span></span> <span data-ttu-id="90fdc-132">Richiede che il tipo di proprietà sia una stringa.</span><span class="sxs-lookup"><span data-stu-id="90fdc-132">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90fdc-133">FilePath</span><span class="sxs-lookup"><span data-stu-id="90fdc-133">FilePath</span></span></td>
<td><span data-ttu-id="90fdc-134">Formatta il valore come percorso di file.</span><span class="sxs-lookup"><span data-stu-id="90fdc-134">Formats the value as a file path.</span></span> <span data-ttu-id="90fdc-135">Nasconde l'estensione in base alle impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="90fdc-135">Hides the extension according to user settings.</span></span> <span data-ttu-id="90fdc-136">Richiede che il tipo di proprietà sia una stringa.</span><span class="sxs-lookup"><span data-stu-id="90fdc-136">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90fdc-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="90fdc-137">Hyperlink</span></span></td>
<td><span data-ttu-id="90fdc-138">Formatta il valore come collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="90fdc-138">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
