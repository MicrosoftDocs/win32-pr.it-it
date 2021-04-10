---
description: 'Specifica il modo in cui IPropertyDescription:: FormatForDisplay deve formattare il valore della proprietà come stringa. Questa operazione è applicabile solo se <displayInfo displayType=&\#0034;DateTime&\#0034;> .'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226893"
---
# <a name="datetimeformat"></a><span data-ttu-id="7281d-104">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="7281d-104">dateTimeFormat</span></span>

<span data-ttu-id="7281d-105">Specifica il modo in cui [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formattare il valore della proprietà come stringa.</span><span class="sxs-lookup"><span data-stu-id="7281d-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="7281d-106">Questa operazione è applicabile solo se <displayInfo displayType="DateTime"> .</span><span class="sxs-lookup"><span data-stu-id="7281d-106">This is applicable only if <displayInfo displayType="DateTime">.</span></span> <span data-ttu-id="7281d-107">Deve essere presente un solo elemento [DateTimeFormat]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="7281d-107">There should be only one [dateTimeFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="7281d-108">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="7281d-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="7281d-109">Se non viene fornito alcun elemento [DateTimeFormat]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="7281d-109">If no [dateTimeFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7281d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7281d-110">Syntax</span></span>


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Month"/>
                <xs:enumeration value="YearMonth"/>
                <xs:enumeration value="Year"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatTimeAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortTime"/>
                <xs:enumeration value="LongTime"/>
                <xs:enumeration value="HideTime"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDateAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortDate"/>
                <xs:enumeration value="LongDate"/>
                <xs:enumeration value="HideDate"/>
                <xs:enumeration value="RelativeShortDate"/>
                <xs:enumeration value="RelativeLongDate"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="7281d-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7281d-111">Element Information</span></span>



| <span data-ttu-id="7281d-112">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="7281d-112">Parent Element</span></span>                                   | <span data-ttu-id="7281d-113">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7281d-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="7281d-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="7281d-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="7281d-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="7281d-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="7281d-116">Attributi</span><span class="sxs-lookup"><span data-stu-id="7281d-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7281d-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="7281d-117">Attribute</span></span></th>
<th><span data-ttu-id="7281d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7281d-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7281d-119">formato</span><span class="sxs-lookup"><span data-stu-id="7281d-119">formatAs</span></span></td>
<td><span data-ttu-id="7281d-120">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="7281d-120">Public.</span></span> <span data-ttu-id="7281d-121">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7281d-121">Optional.</span></span> <span data-ttu-id="7281d-122">Il valore predefinito è &quot; Generale &quot; .</span><span class="sxs-lookup"><span data-stu-id="7281d-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="7281d-123">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="7281d-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7281d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7281d-124">Value</span></span></th>
<th><span data-ttu-id="7281d-125">Significato</span><span class="sxs-lookup"><span data-stu-id="7281d-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7281d-126">Generale</span><span class="sxs-lookup"><span data-stu-id="7281d-126">General</span></span></td>
<td><span data-ttu-id="7281d-127">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7281d-127">Default.</span></span> <span data-ttu-id="7281d-128">Formatta il valore di data e ora usando <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7281d-128">Formats the date-time value using <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>.</span></span> <span data-ttu-id="7281d-129">Usare gli attributi <em>formatTimeAs</em> e <em>formatDateAs</em> per specificare la modalità di formattazione di data e ora.</span><span class="sxs-lookup"><span data-stu-id="7281d-129">Use the <em>formatTimeAs</em> and <em>formatDateAs</em> attributes to specify how the time and date are formatted.</span></span> <span data-ttu-id="7281d-130">Richiede che il tipo di proprietà sia DateTime.</span><span class="sxs-lookup"><span data-stu-id="7281d-130">Requires the property type to be DateTime.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7281d-131">Month</span><span class="sxs-lookup"><span data-stu-id="7281d-131">Month</span></span></td>
<td><span data-ttu-id="7281d-132">Formatta il valore come uno dei mesi dell'anno.</span><span class="sxs-lookup"><span data-stu-id="7281d-132">Formats the value as one of the months of the year.</span></span> <span data-ttu-id="7281d-133">Richiede che il tipo di proprietà sia Int32.</span><span class="sxs-lookup"><span data-stu-id="7281d-133">Requires the property type to be Int32.</span></span> <span data-ttu-id="7281d-134">Il valore deve essere archiviato come valore numerico con 1 che rappresenta il primo mese dell'anno.</span><span class="sxs-lookup"><span data-stu-id="7281d-134">The value must be stored as a numeric value with 1 representing the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7281d-135">YearMonth</span><span class="sxs-lookup"><span data-stu-id="7281d-135">YearMonth</span></span></td>
<td><span data-ttu-id="7281d-136">Formatta il valore come &quot; anno mese &quot; .</span><span class="sxs-lookup"><span data-stu-id="7281d-136">Formats the value as &quot;Year - Month&quot;.</span></span> <span data-ttu-id="7281d-137">Richiede che il tipo di proprietà sia Int32.</span><span class="sxs-lookup"><span data-stu-id="7281d-137">Requires the property type to be Int32.</span></span> <span data-ttu-id="7281d-138">Il valore deve essere archiviato in modo che i due byte più elevati specifichino l'anno e i due byte più bassi specifichino il mese.</span><span class="sxs-lookup"><span data-stu-id="7281d-138">The value must be stored such that the two highest bytes specify the year and the lower two bytes specify the month.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7281d-139">Year</span><span class="sxs-lookup"><span data-stu-id="7281d-139">Year</span></span></td>
<td><span data-ttu-id="7281d-140">Formatta il valore come stringa semplice.</span><span class="sxs-lookup"><span data-stu-id="7281d-140">Formats the value as a simple string.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7281d-141">formatTimeAs</span><span class="sxs-lookup"><span data-stu-id="7281d-141">formatTimeAs</span></span></td>
<td><span data-ttu-id="7281d-142">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="7281d-142">Public.</span></span> <span data-ttu-id="7281d-143">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7281d-143">Optional.</span></span> <span data-ttu-id="7281d-144">Il valore predefinito è &quot; ShortTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="7281d-144">Default is &quot;ShortTime&quot;.</span></span> <span data-ttu-id="7281d-145">Specifica il formato in cui visualizzare l'ora.</span><span class="sxs-lookup"><span data-stu-id="7281d-145">Specifies the format in which to display time.</span></span> <span data-ttu-id="7281d-146">Si applica quando <strong>formats &quot; = &quot; General</strong>.</span><span class="sxs-lookup"><span data-stu-id="7281d-146">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="7281d-147">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="7281d-147">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7281d-148">Valore</span><span class="sxs-lookup"><span data-stu-id="7281d-148">Value</span></span></th>
<th><span data-ttu-id="7281d-149">Significato</span><span class="sxs-lookup"><span data-stu-id="7281d-149">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7281d-150">ShortTime</span><span class="sxs-lookup"><span data-stu-id="7281d-150">ShortTime</span></span></td>
<td><span data-ttu-id="7281d-151">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7281d-151">Default.</span></span> <span data-ttu-id="7281d-152">Mostra l'ora, ad esempio &quot; 7:48 PM &quot; .</span><span class="sxs-lookup"><span data-stu-id="7281d-152">Show the time like &quot;7:48 PM&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7281d-153">Lunga</span><span class="sxs-lookup"><span data-stu-id="7281d-153">LongTime</span></span></td>
<td><span data-ttu-id="7281d-154">Mostra l'ora, ad esempio &quot; 7:48:33 PM &quot; .</span><span class="sxs-lookup"><span data-stu-id="7281d-154">Show the time like &quot;7:48:33 PM&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7281d-155">HideTime</span><span class="sxs-lookup"><span data-stu-id="7281d-155">HideTime</span></span></td>
<td><span data-ttu-id="7281d-156">Non visualizzare la parte relativa all'ora della data.</span><span class="sxs-lookup"><span data-stu-id="7281d-156">Do not display the time portion of the date.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7281d-157">formatDateAs</span><span class="sxs-lookup"><span data-stu-id="7281d-157">formatDateAs</span></span></td>
<td><span data-ttu-id="7281d-158">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="7281d-158">Public.</span></span> <span data-ttu-id="7281d-159">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7281d-159">Optional.</span></span> <span data-ttu-id="7281d-160">Il valore predefinito è &quot; shortdate &quot; .</span><span class="sxs-lookup"><span data-stu-id="7281d-160">Default is &quot;ShortDate&quot;.</span></span> <span data-ttu-id="7281d-161">Specifica il formato in cui visualizzare la data.</span><span class="sxs-lookup"><span data-stu-id="7281d-161">Specifies the format in which to display the date.</span></span> <span data-ttu-id="7281d-162">Si applica quando <strong>formats &quot; = &quot; General</strong>.</span><span class="sxs-lookup"><span data-stu-id="7281d-162">Applies when <strong>formatAs=&quot;General&quot;</strong>.</span></span> <span data-ttu-id="7281d-163">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="7281d-163">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7281d-164">Valore</span><span class="sxs-lookup"><span data-stu-id="7281d-164">Value</span></span></th>
<th><span data-ttu-id="7281d-165">Esempio</span><span class="sxs-lookup"><span data-stu-id="7281d-165">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7281d-166">ShortDate</span><span class="sxs-lookup"><span data-stu-id="7281d-166">ShortDate</span></span></td>
<td><span data-ttu-id="7281d-167">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7281d-167">Default.</span></span> <span data-ttu-id="7281d-168">Mostra la data, ad esempio &quot; 5/13/59 &quot; .</span><span class="sxs-lookup"><span data-stu-id="7281d-168">Show the date like &quot;5/13/59&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7281d-169">LongDate</span><span class="sxs-lookup"><span data-stu-id="7281d-169">LongDate</span></span></td>
<td><span data-ttu-id="7281d-170">Mostra la data come &quot; mercoledì, 13 maggio 1959 &quot; .</span><span class="sxs-lookup"><span data-stu-id="7281d-170">Show the date like &quot;Wednesday, May 13, 1959&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7281d-171">HideDate</span><span class="sxs-lookup"><span data-stu-id="7281d-171">HideDate</span></span></td>
<td><span data-ttu-id="7281d-172">Non visualizzare la parte relativa alla data.</span><span class="sxs-lookup"><span data-stu-id="7281d-172">Do not display the date portion.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7281d-173">RelativeShortDate</span><span class="sxs-lookup"><span data-stu-id="7281d-173">RelativeShortDate</span></span></td>
<td><span data-ttu-id="7281d-174">Mostra la data come &quot; shortdate &quot; , ma usa le descrizioni relative, ad esempio &quot; ieri &quot; , quando possibile.</span><span class="sxs-lookup"><span data-stu-id="7281d-174">Show the date like &quot;ShortDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7281d-175">RelativeLongDate</span><span class="sxs-lookup"><span data-stu-id="7281d-175">RelativeLongDate</span></span></td>
<td><span data-ttu-id="7281d-176">Mostra la data come &quot; LongDate &quot; , ma usa le descrizioni relative, ad esempio &quot; ieri &quot; , quando possibile.</span><span class="sxs-lookup"><span data-stu-id="7281d-176">Show the date like &quot;LongDate&quot;, but use relative descriptions, such as &quot;yesterday&quot;, whenever possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
