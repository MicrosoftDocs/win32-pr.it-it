---
description: 'Specifica il modo in cui IPropertyDescription:: FormatForDisplay deve formattare il valore della proprietà come stringa. Questa operazione è applicabile solo se <displayInfo displayType=&\#0034;Number&\#0034;> .'
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: numberFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750a9fb4dcf6a7a56c350fccf80241644b956da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310120"
---
# <a name="numberformat"></a><span data-ttu-id="59b38-104">numberFormat</span><span class="sxs-lookup"><span data-stu-id="59b38-104">numberFormat</span></span>

<span data-ttu-id="59b38-105">Specifica il modo in cui [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formattare il valore della proprietà come stringa.</span><span class="sxs-lookup"><span data-stu-id="59b38-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="59b38-106">Questa operazione è applicabile solo se <displayInfo displayType="Number"> .</span><span class="sxs-lookup"><span data-stu-id="59b38-106">This is applicable only if <displayInfo displayType="Number">.</span></span> <span data-ttu-id="59b38-107">Deve essere presente un solo elemento [NumberFormat]() per ogni elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="59b38-107">There should be only one [numberFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="59b38-108">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="59b38-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="59b38-109">Se non viene fornito alcun elemento [NumberFormat]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="59b38-109">If no [numberFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b38-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59b38-110">Syntax</span></span>


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Percentage"/>
                <xs:enumeration value="ByteSize"/>
                <xs:enumeration value="KBSize"/>
                <xs:enumeration value="SampleSize"/>
                <xs:enumeration value="Bitrate"/>
                <xs:enumeration value="SampleRate"/>
                <xs:enumeration value="FrameRate"/>
                <xs:enumeration value="Pixels"/>
                <xs:enumeration value="DPI"/>
                <xs:enumeration value="Duration"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDurationAs">
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="59b38-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="59b38-111">Element Information</span></span>



| <span data-ttu-id="59b38-112">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="59b38-112">Parent Element</span></span>                                   | <span data-ttu-id="59b38-113">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="59b38-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="59b38-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="59b38-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="59b38-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="59b38-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="59b38-116">Attributi</span><span class="sxs-lookup"><span data-stu-id="59b38-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59b38-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="59b38-117">Attribute</span></span></th>
<th><span data-ttu-id="59b38-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59b38-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59b38-119">formato</span><span class="sxs-lookup"><span data-stu-id="59b38-119">formatAs</span></span></td>
<td><span data-ttu-id="59b38-120">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="59b38-120">Public.</span></span> <span data-ttu-id="59b38-121">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="59b38-121">Optional.</span></span> <span data-ttu-id="59b38-122">Il valore predefinito è &quot; Generale &quot; .</span><span class="sxs-lookup"><span data-stu-id="59b38-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="59b38-123">Specifica il formato di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="59b38-123">Specifies the display format.</span></span> <span data-ttu-id="59b38-124">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="59b38-124">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="59b38-125">Valore</span><span class="sxs-lookup"><span data-stu-id="59b38-125">Value</span></span></th>
<th><span data-ttu-id="59b38-126">Significato</span><span class="sxs-lookup"><span data-stu-id="59b38-126">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59b38-127">Generale</span><span class="sxs-lookup"><span data-stu-id="59b38-127">General</span></span></td>
<td><span data-ttu-id="59b38-128">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="59b38-128">Default.</span></span> <span data-ttu-id="59b38-129">Visualizza il valore come numero non formattato.</span><span class="sxs-lookup"><span data-stu-id="59b38-129">Displays the value as an unformatted number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b38-130">Percentuale</span><span class="sxs-lookup"><span data-stu-id="59b38-130">Percentage</span></span></td>
<td><span data-ttu-id="59b38-131">Formatta il valore come percentuale.</span><span class="sxs-lookup"><span data-stu-id="59b38-131">Formats the value as a percentage.</span></span> <span data-ttu-id="59b38-132">Richiede che la proprietà sia UInt32.</span><span class="sxs-lookup"><span data-stu-id="59b38-132">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59b38-133">ByteSize</span><span class="sxs-lookup"><span data-stu-id="59b38-133">ByteSize</span></span></td>
<td><span data-ttu-id="59b38-134">Formatta il valore come byte, &quot; KB &quot; , &quot; MB &quot; o GB a &quot; seconda dei &quot; casi.</span><span class="sxs-lookup"><span data-stu-id="59b38-134">Formats the value as a byte, &quot;KB&quot;, &quot;MB&quot;, or &quot;GB&quot; as appropriate.</span></span> <span data-ttu-id="59b38-135">Richiede che la proprietà sia UInt64.</span><span class="sxs-lookup"><span data-stu-id="59b38-135">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b38-136">KBSize</span><span class="sxs-lookup"><span data-stu-id="59b38-136">KBSize</span></span></td>
<td><span data-ttu-id="59b38-137">Formatta il valore come &quot; KB &quot; , indipendentemente dal valore.</span><span class="sxs-lookup"><span data-stu-id="59b38-137">Formats the value as a &quot;KB&quot;, no matter what the value is.</span></span> <span data-ttu-id="59b38-138">Richiede che la proprietà sia UInt64.</span><span class="sxs-lookup"><span data-stu-id="59b38-138">Requires the property to be UInt64.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59b38-139">SampleSize</span><span class="sxs-lookup"><span data-stu-id="59b38-139">SampleSize</span></span></td>
<td><span data-ttu-id="59b38-140">Formatta il valore come numero di bit.</span><span class="sxs-lookup"><span data-stu-id="59b38-140">Formats the value as a number of bits.</span></span> <span data-ttu-id="59b38-141">Richiede che la proprietà sia UInt32.</span><span class="sxs-lookup"><span data-stu-id="59b38-141">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b38-142">Velocità in bit</span><span class="sxs-lookup"><span data-stu-id="59b38-142">BitRate</span></span></td>
<td><span data-ttu-id="59b38-143">Formatta il valore in &quot; Kbps &quot; .</span><span class="sxs-lookup"><span data-stu-id="59b38-143">Formats the value in &quot;Kbps&quot;.</span></span> <span data-ttu-id="59b38-144">Richiede che la proprietà sia UInt32.</span><span class="sxs-lookup"><span data-stu-id="59b38-144">Requires the property to be UInt32.</span></span> <span data-ttu-id="59b38-145">Il valore deve essere archiviato in &quot; unità bits al secondo &quot; .</span><span class="sxs-lookup"><span data-stu-id="59b38-145">The value must be stored in &quot;bits-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59b38-146">SampleRate</span><span class="sxs-lookup"><span data-stu-id="59b38-146">SampleRate</span></span></td>
<td><span data-ttu-id="59b38-147">Formatta il valore in &quot; kHz &quot; .</span><span class="sxs-lookup"><span data-stu-id="59b38-147">Formats the value in &quot;KHz&quot;.</span></span> <span data-ttu-id="59b38-148">Richiede che la proprietà sia UInt32.</span><span class="sxs-lookup"><span data-stu-id="59b38-148">Requires the property to be UInt32.</span></span> <span data-ttu-id="59b38-149">Il valore deve essere archiviato in &quot; &quot; unità Hertz.</span><span class="sxs-lookup"><span data-stu-id="59b38-149">The value must be stored in &quot;Hertz&quot; units.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b38-150">FrameRate</span><span class="sxs-lookup"><span data-stu-id="59b38-150">FrameRate</span></span></td>
<td><span data-ttu-id="59b38-151">Formatta il valore in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="59b38-151">Formats the value in frames/second.</span></span> <span data-ttu-id="59b38-152">Richiede che la proprietà sia UInt32.</span><span class="sxs-lookup"><span data-stu-id="59b38-152">Requires the property to be UInt32.</span></span> <span data-ttu-id="59b38-153">Il valore deve essere archiviato in &quot; unità con frame kilo al secondo &quot; .</span><span class="sxs-lookup"><span data-stu-id="59b38-153">The value must be stored in &quot;kilo-frames-per-second&quot; units.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59b38-154">Pixel</span><span class="sxs-lookup"><span data-stu-id="59b38-154">Pixels</span></span></td>
<td><span data-ttu-id="59b38-155">Formatta il valore in unità pixel.</span><span class="sxs-lookup"><span data-stu-id="59b38-155">Formats the value in pixel units.</span></span> <span data-ttu-id="59b38-156">Richiede che la proprietà sia UInt32.</span><span class="sxs-lookup"><span data-stu-id="59b38-156">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b38-157">DPI</span><span class="sxs-lookup"><span data-stu-id="59b38-157">DPI</span></span></td>
<td><span data-ttu-id="59b38-158">Formatta il valore in punti per pollice.</span><span class="sxs-lookup"><span data-stu-id="59b38-158">Formats the value in dots-per-inch.</span></span> <span data-ttu-id="59b38-159">Richiede che la proprietà sia UInt32.</span><span class="sxs-lookup"><span data-stu-id="59b38-159">Requires the property to be UInt32.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59b38-160">Duration</span><span class="sxs-lookup"><span data-stu-id="59b38-160">Duration</span></span></td>
<td><span data-ttu-id="59b38-161">Formatta il valore come Duration.</span><span class="sxs-lookup"><span data-stu-id="59b38-161">Formats the value as a duration.</span></span> <span data-ttu-id="59b38-162">Usare <formatDurationAs> per specificare il formato della durata.</span><span class="sxs-lookup"><span data-stu-id="59b38-162">Use <formatDurationAs> to specify the duration format.</span></span> <span data-ttu-id="59b38-163">Richiede che la proprietà sia UInt64.</span><span class="sxs-lookup"><span data-stu-id="59b38-163">Requires the property to be UInt64.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b38-164">formatDurationAs</span><span class="sxs-lookup"><span data-stu-id="59b38-164">formatDurationAs</span></span></td>
<td><span data-ttu-id="59b38-165">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="59b38-165">Public.</span></span> <span data-ttu-id="59b38-166">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="59b38-166">Optional.</span></span> <span data-ttu-id="59b38-167">Il valore predefinito è &quot; hh: mm: SS &quot; .</span><span class="sxs-lookup"><span data-stu-id="59b38-167">Default is &quot;hh:mm:ss&quot;.</span></span> <span data-ttu-id="59b38-168">Si applica solo se <em>formats &quot; = &quot; Duration</em>.</span><span class="sxs-lookup"><span data-stu-id="59b38-168">Only applies if <em>formatAs=&quot;Duration&quot;</em>.</span></span> <span data-ttu-id="59b38-169">Richiede che la proprietà sia UInt64.</span><span class="sxs-lookup"><span data-stu-id="59b38-169">Requires the property to be UInt64.</span></span> <span data-ttu-id="59b38-170">I valori validi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="59b38-170">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="59b38-171">Valore</span><span class="sxs-lookup"><span data-stu-id="59b38-171">Value</span></span></th>
<th><span data-ttu-id="59b38-172">Significato</span><span class="sxs-lookup"><span data-stu-id="59b38-172">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59b38-173">hh:mm</span><span class="sxs-lookup"><span data-stu-id="59b38-173">hh:mm</span></span></td>
<td><span data-ttu-id="59b38-174">Formatta il valore in ore e minuti.</span><span class="sxs-lookup"><span data-stu-id="59b38-174">Formats the value in hours and minutes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b38-175">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="59b38-175">hh:mm:ss</span></span></td>
<td><span data-ttu-id="59b38-176">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="59b38-176">Default.</span></span> <span data-ttu-id="59b38-177">Formatta il valore in ore, minuti e secondi.</span><span class="sxs-lookup"><span data-stu-id="59b38-177">Formats the value in hours, minutes, and seconds.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59b38-178">HH: mm: SS. fff</span><span class="sxs-lookup"><span data-stu-id="59b38-178">hh:mm:ss.fff</span></span></td>
<td><span data-ttu-id="59b38-179">Formatta il valore in ore, minuti, secondi e millisecondi.</span><span class="sxs-lookup"><span data-stu-id="59b38-179">Formats the value in hours, minutes, seconds, and milliseconds.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
