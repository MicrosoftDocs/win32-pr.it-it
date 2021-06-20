---
description: Specifica il modo in cui IPropertyDescription::FormatForDisplay deve formattare il valore della proprietà stringFormat come stringa.
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730355507b78d99eba02e82666427dd29425c942
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408354"
---
# <a name="stringformat"></a><span data-ttu-id="1c03e-103">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1c03e-103">stringFormat</span></span>

<span data-ttu-id="1c03e-104">Specifica il modo [**in cui IPropertyDescription::FormatForDisplay deve**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) formattare il valore della proprietà come stringa.</span><span class="sxs-lookup"><span data-stu-id="1c03e-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="1c03e-105">Questa opzione è applicabile solo se <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="1c03e-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="1c03e-106">Deve essere presente un solo [elemento stringFormat]() per ogni [elemento displayInfo.](./propdesc-schema-displayinfo.md)</span><span class="sxs-lookup"><span data-stu-id="1c03e-106">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="1c03e-107">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="1c03e-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="1c03e-108">Se non viene [specificato alcun elemento stringFormat,]() le impostazioni dell'attributo predefinite vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c03e-108">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c03e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c03e-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="1c03e-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1c03e-110">Element Information</span></span>



| <span data-ttu-id="1c03e-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1c03e-111">Parent Element</span></span>                                   | <span data-ttu-id="1c03e-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1c03e-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="1c03e-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1c03e-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="1c03e-114">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1c03e-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="1c03e-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="1c03e-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c03e-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="1c03e-116">Attribute</span></span></th>
<th><span data-ttu-id="1c03e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c03e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c03e-118">formatAs</span><span class="sxs-lookup"><span data-stu-id="1c03e-118">formatAs</span></span></td>
<td><span data-ttu-id="1c03e-119">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="1c03e-119">Public.</span></span> <span data-ttu-id="1c03e-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1c03e-120">Optional.</span></span> <span data-ttu-id="1c03e-121">Il valore predefinito è &quot; &quot; Generale.</span><span class="sxs-lookup"><span data-stu-id="1c03e-121">Default is &quot;General&quot;.</span></span> <span data-ttu-id="1c03e-122">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="1c03e-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c03e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1c03e-123">Value</span></span></th>
<th><span data-ttu-id="1c03e-124">Significato</span><span class="sxs-lookup"><span data-stu-id="1c03e-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c03e-125">Generale</span><span class="sxs-lookup"><span data-stu-id="1c03e-125">General</span></span></td>
<td><span data-ttu-id="1c03e-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1c03e-126">Default.</span></span> <span data-ttu-id="1c03e-127">Restituisce il valore come stringa non formattata.</span><span class="sxs-lookup"><span data-stu-id="1c03e-127">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c03e-128">FileName</span><span class="sxs-lookup"><span data-stu-id="1c03e-128">FileName</span></span></td>
<td><span data-ttu-id="1c03e-129">Formatta il valore come nome file.</span><span class="sxs-lookup"><span data-stu-id="1c03e-129">Formats the value as a file name.</span></span> <span data-ttu-id="1c03e-130">Nasconde l'estensione in base alle impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="1c03e-130">Hides the extension according to user settings.</span></span> <span data-ttu-id="1c03e-131">Richiede che il tipo di proprietà sia String.</span><span class="sxs-lookup"><span data-stu-id="1c03e-131">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c03e-132">FilePath</span><span class="sxs-lookup"><span data-stu-id="1c03e-132">FilePath</span></span></td>
<td><span data-ttu-id="1c03e-133">Formatta il valore come percorso di file.</span><span class="sxs-lookup"><span data-stu-id="1c03e-133">Formats the value as a file path.</span></span> <span data-ttu-id="1c03e-134">Nasconde l'estensione in base alle impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="1c03e-134">Hides the extension according to user settings.</span></span> <span data-ttu-id="1c03e-135">Richiede che il tipo di proprietà sia String.</span><span class="sxs-lookup"><span data-stu-id="1c03e-135">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c03e-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="1c03e-136">Hyperlink</span></span></td>
<td><span data-ttu-id="1c03e-137">Formatta il valore come collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="1c03e-137">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
