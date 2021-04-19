---
description: Specifica le informazioni di visualizzazione di una proprietà.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: displayInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff0bb441b4535c0b6c6f3183671fbe8ade09183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312553"
---
# <a name="displayinfo"></a><span data-ttu-id="5511b-103">displayInfo</span><span class="sxs-lookup"><span data-stu-id="5511b-103">displayInfo</span></span>

<span data-ttu-id="5511b-104">Specifica le informazioni di visualizzazione di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="5511b-104">Specifies a property's display information.</span></span> <span data-ttu-id="5511b-105">Deve essere presente un solo elemento [displayInfo]() per ogni [PropertyDescription](./propdesc-schema-propertydescription.md).</span><span class="sxs-lookup"><span data-stu-id="5511b-105">There should be only one [displayInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span>

<span data-ttu-id="5511b-106">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="5511b-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="5511b-107">Se non viene specificato alcun elemento [displayInfo]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="5511b-107">If no [displayInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5511b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5511b-108">Syntax</span></span>


```
<!-- displayInfo -->
<xs:element name="displayInfo">
    <xs:complexType>
        <xs:all>
            <xs:element name="stringFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="booleanFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="numberFormat" minOccurs="0" maxOccurs="1">
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
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="hh:mm"/>
                                <xs:enumeration value="hh:mm:ss"/>
                                <xs:enumeration value="hh:mm:ss.fff"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="dateTimeFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="enumeratedList" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="value" type="xs:string" use="required"/>
                                <xs:attribute name="text" type="xs:string" use="required"/>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="minValue" type="xs:string" use="required"/>
                                <xs:attribute name="setValue" type="xs:string"/>
                                <xs:attribute name="text" type="xs:string"/>
                            </xs:complexType>
                        </xs:element>
                    </xs:sequence>

                    <xs:attribute name="defaultText" type="xs:string"/>
                    <xs:attribute name="useValueForDefault" type="xs:boolean"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="drawControl" minOccurs="0" maxOccurs="1">
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
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="editControl" minOccurs="0" maxOccurs="1">
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
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="filterControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="Rating"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="queryControl" minOccurs="0" maxOccurs="1">
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
        </xs:all>

        <xs:attribute name="defaultColumnWidth" type="xs:nonNegativeInteger" default="20"/>
        <xs:attribute name="displayType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        
        <xs:attribute name="alignment" default="Left">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Left"/>
                    <xs:enumeration value="Center"/>
                    <xs:enumeration value="Right"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="relativeDescriptionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Count"/>
                    <xs:enumeration value="Revision"/>
                    <xs:enumeration value="Length"/>
                    <xs:enumeration value="Duration"/>
                    <xs:enumeration value="Speed"/>
                    <xs:enumeration value="Rate"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Priority"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultSortDirection" default="Ascending">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                  <xs:enumeration value="Ascending"/>
                  <xs:enumeration value="Descending"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="5511b-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5511b-109">Element Information</span></span>



| <span data-ttu-id="5511b-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="5511b-110">Parent Element</span></span>                                                   | <span data-ttu-id="5511b-111">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5511b-111">Child Elements</span></span>                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5511b-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="5511b-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="5511b-113">stringFormat</span><span class="sxs-lookup"><span data-stu-id="5511b-113">stringFormat</span></span>](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [<span data-ttu-id="5511b-114">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="5511b-114">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [<span data-ttu-id="5511b-115">numberFormat</span><span class="sxs-lookup"><span data-stu-id="5511b-115">numberFormat</span></span>](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [<span data-ttu-id="5511b-116">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5511b-116">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [<span data-ttu-id="5511b-117">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="5511b-117">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [<span data-ttu-id="5511b-118">drawControl</span><span class="sxs-lookup"><span data-stu-id="5511b-118">drawControl</span></span>](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="5511b-119">editControl</span><span class="sxs-lookup"><span data-stu-id="5511b-119">editControl</span></span>](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [<span data-ttu-id="5511b-120">filterControl</span><span class="sxs-lookup"><span data-stu-id="5511b-120">filterControl</span></span>](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | <span data-ttu-id="5511b-121">[queryControl](./propdesc-schema-querycontrol.md) (solo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5511b-121">[queryControl](./propdesc-schema-querycontrol.md) (Windows Vista only.</span></span> <span data-ttu-id="5511b-122">Non supportato in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5511b-122">Not supported in Windows 7 and later.)</span></span> |



 

## <a name="attributes"></a><span data-ttu-id="5511b-123">Attributi</span><span class="sxs-lookup"><span data-stu-id="5511b-123">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5511b-124">Attributo</span><span class="sxs-lookup"><span data-stu-id="5511b-124">Attribute</span></span></th>
<th><span data-ttu-id="5511b-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5511b-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5511b-126">defaultColumnWidth</span><span class="sxs-lookup"><span data-stu-id="5511b-126">defaultColumnWidth</span></span></td>
<td><span data-ttu-id="5511b-127">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="5511b-127">Public.</span></span> <span data-ttu-id="5511b-128">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5511b-128">Optional.</span></span> <span data-ttu-id="5511b-129">Il valore predefinito è &quot; 20 &quot; .</span><span class="sxs-lookup"><span data-stu-id="5511b-129">Default is &quot;20&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5511b-130">displayType</span><span class="sxs-lookup"><span data-stu-id="5511b-130">displayType</span></span></td>
<td><span data-ttu-id="5511b-131">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="5511b-131">Public.</span></span> <span data-ttu-id="5511b-132">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5511b-132">Optional.</span></span> <span data-ttu-id="5511b-133">Il valore predefinito è &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="5511b-133">Default is &quot;String&quot;.</span></span> <span data-ttu-id="5511b-134">Specifica il tipo della stringa di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="5511b-134">Specifies the type of the display string.</span></span> <span data-ttu-id="5511b-135">Una volta impostati qui, i valori <strong>PROPDESC_DISPLAYTYPE</strong> associati vengono recuperati da <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription:: GetDisplayType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5511b-135">Once set here, the associated <strong>PROPDESC_DISPLAYTYPE</strong> values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription::GetDisplayType</strong></a>.</span></span> <span data-ttu-id="5511b-136">Di seguito sono riportati i tipi validi.</span><span class="sxs-lookup"><span data-stu-id="5511b-136">The following are valid types.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5511b-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5511b-137">Value</span></span></th>
<th><span data-ttu-id="5511b-138">Significato</span><span class="sxs-lookup"><span data-stu-id="5511b-138">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5511b-139">string</span><span class="sxs-lookup"><span data-stu-id="5511b-139">String</span></span></td>
<td><span data-ttu-id="5511b-140">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5511b-140">Default.</span></span> <span data-ttu-id="5511b-141">Il valore viene visualizzato sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="5511b-141">Value is displayed as a string.</span></span> <span data-ttu-id="5511b-142">Usare &quot; StringFormat &quot; per formattare.</span><span class="sxs-lookup"><span data-stu-id="5511b-142">Use &quot;stringFormat&quot; to format.</span></span> <span data-ttu-id="5511b-143">Il metodo restituisce PDDT_STRING.</span><span class="sxs-lookup"><span data-stu-id="5511b-143">Method returns PDDT_STRING.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5511b-144">Number</span><span class="sxs-lookup"><span data-stu-id="5511b-144">Number</span></span></td>
<td><span data-ttu-id="5511b-145">Valore predefinito per le proprietà numeriche.</span><span class="sxs-lookup"><span data-stu-id="5511b-145">Default for numeric properties.</span></span> <span data-ttu-id="5511b-146">Il valore viene visualizzato sotto forma di numero.</span><span class="sxs-lookup"><span data-stu-id="5511b-146">Value is displayed as a number.</span></span> <span data-ttu-id="5511b-147">Usare &quot; NumberFormat &quot; per formattare.</span><span class="sxs-lookup"><span data-stu-id="5511b-147">Use &quot;numberFormat&quot; to format.</span></span> <span data-ttu-id="5511b-148">Il metodo restituisce PDDT_NUMBER.</span><span class="sxs-lookup"><span data-stu-id="5511b-148">Method returns PDDT_NUMBER.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5511b-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="5511b-149">Boolean</span></span></td>
<td><span data-ttu-id="5511b-150">Valore predefinito se <typeInfo type=&quot;Boolean&quot;> .</span><span class="sxs-lookup"><span data-stu-id="5511b-150">Default if <typeInfo type=&quot;Boolean&quot;>.</span></span> <span data-ttu-id="5511b-151">Il valore viene visualizzato come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="5511b-151">Value is displayed as a boolean.</span></span> <span data-ttu-id="5511b-152">Usare &quot; booleanFormat &quot; per formattare.</span><span class="sxs-lookup"><span data-stu-id="5511b-152">Use &quot;booleanFormat&quot; to format.</span></span> <span data-ttu-id="5511b-153">Il metodo restituisce PDDT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="5511b-153">Method returns PDDT_BOOLEAN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5511b-154">Datetime</span><span class="sxs-lookup"><span data-stu-id="5511b-154">DateTime</span></span></td>
<td><span data-ttu-id="5511b-155">Valore predefinito se <typeInfo type=&quot;DateTime&quot;> .</span><span class="sxs-lookup"><span data-stu-id="5511b-155">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="5511b-156">Il valore viene visualizzato come data o ora.</span><span class="sxs-lookup"><span data-stu-id="5511b-156">Value is displayed as a date or time.</span></span> <span data-ttu-id="5511b-157">Utilizzare &quot; dateTimeFormat &quot; per formattare.</span><span class="sxs-lookup"><span data-stu-id="5511b-157">Use &quot;dateTimeFormat&quot; to format.</span></span> <span data-ttu-id="5511b-158">Il metodo restituisce PDDT_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="5511b-158">Method returns PDDT_DATETIME.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5511b-159">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="5511b-159">Enumeration</span></span></td>
<td><span data-ttu-id="5511b-160">Il valore viene visualizzato come mapping della stringa di visualizzazione fornito &quot; dall' &quot; elemento enumeratedList.</span><span class="sxs-lookup"><span data-stu-id="5511b-160">Value is displayed as a display string mapping provided by the &quot;enumeratedList&quot; element.</span></span> <span data-ttu-id="5511b-161">Il metodo restituisce PDDT_ENUMERATED.</span><span class="sxs-lookup"><span data-stu-id="5511b-161">Method returns PDDT_ENUMERATED.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5511b-162">allineamento</span><span class="sxs-lookup"><span data-stu-id="5511b-162">alignment</span></span></td>
<td><span data-ttu-id="5511b-163">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5511b-163">Optional.</span></span> <span data-ttu-id="5511b-164">Il valore predefinito è &quot; Left &quot; .</span><span class="sxs-lookup"><span data-stu-id="5511b-164">Default is &quot;Left&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5511b-165">Valore</span><span class="sxs-lookup"><span data-stu-id="5511b-165">Value</span></span></th>
<th><span data-ttu-id="5511b-166">Significato</span><span class="sxs-lookup"><span data-stu-id="5511b-166">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5511b-167">Sinistra</span><span class="sxs-lookup"><span data-stu-id="5511b-167">Left</span></span></td>
<td><span data-ttu-id="5511b-168">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5511b-168">Default.</span></span> <span data-ttu-id="5511b-169">Allinea a sinistra.</span><span class="sxs-lookup"><span data-stu-id="5511b-169">Align left.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5511b-170">Center</span><span class="sxs-lookup"><span data-stu-id="5511b-170">Center</span></span></td>
<td><span data-ttu-id="5511b-171">Allinea al centro.</span><span class="sxs-lookup"><span data-stu-id="5511b-171">Align center.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5511b-172">Destra</span><span class="sxs-lookup"><span data-stu-id="5511b-172">Right</span></span></td>
<td><span data-ttu-id="5511b-173">Allinea a destra.</span><span class="sxs-lookup"><span data-stu-id="5511b-173">Align right.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5511b-174">relativeDescriptionType</span><span class="sxs-lookup"><span data-stu-id="5511b-174">relativeDescriptionType</span></span></td>
<td><span data-ttu-id="5511b-175">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5511b-175">Optional.</span></span> <span data-ttu-id="5511b-176">Il valore predefinito è &quot; Generale &quot; .</span><span class="sxs-lookup"><span data-stu-id="5511b-176">Default is &quot;General&quot;.</span></span> <span data-ttu-id="5511b-177">Specifica il modo in cui devono essere descritti due valori di questa proprietà quando vengono confrontati tra loro.</span><span class="sxs-lookup"><span data-stu-id="5511b-177">Specifies how two values of this property should be described when they are compared with one another.</span></span> <span data-ttu-id="5511b-178">In caso di equivalenza, &quot; &quot; viene sempre usato lo stesso.</span><span class="sxs-lookup"><span data-stu-id="5511b-178">In the case of equivalency, &quot;Same&quot; is always used.</span></span> <span data-ttu-id="5511b-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription:: GetRelativeDescription</strong></a> e <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription:: GetRelativeDescriptionType</strong></a> usano questo valore per determinare quale descrizione relativa Visualizza i nomi da usare.</span><span class="sxs-lookup"><span data-stu-id="5511b-179"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription::GetRelativeDescription</strong></a> and <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription::GetRelativeDescriptionType</strong></a> use this value to determine what relative description display names to use.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5511b-180">Valore</span><span class="sxs-lookup"><span data-stu-id="5511b-180">Value</span></span></th>
<th><span data-ttu-id="5511b-181">Significato</span><span class="sxs-lookup"><span data-stu-id="5511b-181">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5511b-182">Generale</span><span class="sxs-lookup"><span data-stu-id="5511b-182">General</span></span></td>
<td><span data-ttu-id="5511b-183">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5511b-183">Default.</span></span> <span data-ttu-id="5511b-184">USA &quot; &quot;  /  &quot; lo stesso &quot;  /  &quot; diverso &quot; .</span><span class="sxs-lookup"><span data-stu-id="5511b-184">Uses &quot;Different&quot; / &quot;Same&quot; / &quot;Different&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5511b-185">Data</span><span class="sxs-lookup"><span data-stu-id="5511b-185">Date</span></span></td>
<td><span data-ttu-id="5511b-186">Valore predefinito se <typeInfo type=&quot;DateTime&quot;> .</span><span class="sxs-lookup"><span data-stu-id="5511b-186">Default if <typeInfo type=&quot;DateTime&quot;>.</span></span> <span data-ttu-id="5511b-187">USA &quot; &quot;  /  &quot; lo stesso in un &quot;  /  &quot; secondo momento &quot; o usa &quot; &quot;  /  &quot; lo stesso più &quot;  /  &quot; recente &quot; o USA prima di tutto &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="5511b-187">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;, or uses &quot;Older&quot; / &quot;Same&quot; / &quot;Newer&quot;, or uses &quot;Sooner&quot; / &quot;Same&quot; / &quot;Later&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5511b-188">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5511b-188">Size</span></span></td>
<td><span data-ttu-id="5511b-189">USA &quot; &quot;  /  &quot; lo stesso più &quot;  /  &quot; grande&quot;</span><span class="sxs-lookup"><span data-stu-id="5511b-189">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5511b-190">Conteggio</span><span class="sxs-lookup"><span data-stu-id="5511b-190">Count</span></span></td>
<td><span data-ttu-id="5511b-191">USA &quot; &quot;  /  &quot; lo stesso più &quot;  /  &quot; grande&quot;</span><span class="sxs-lookup"><span data-stu-id="5511b-191">Uses &quot;Smaller&quot; / &quot;Same&quot; / &quot;Larger&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5511b-192">Revisione</span><span class="sxs-lookup"><span data-stu-id="5511b-192">Revision</span></span></td>
<td><span data-ttu-id="5511b-193">USA &quot; precedenti &quot;  /  &quot; allo stesso &quot;  /  &quot; momento&quot;</span><span class="sxs-lookup"><span data-stu-id="5511b-193">Uses &quot;Earlier&quot; / &quot;Same&quot; / &quot;Later&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5511b-194">Length</span><span class="sxs-lookup"><span data-stu-id="5511b-194">Length</span></span></td>
<td><span data-ttu-id="5511b-195">USA &quot; più breve &quot;  /  &quot; lo stesso &quot;  /  &quot; più a lungo&quot;</span><span class="sxs-lookup"><span data-stu-id="5511b-195">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5511b-196">Duration</span><span class="sxs-lookup"><span data-stu-id="5511b-196">Duration</span></span></td>
<td><span data-ttu-id="5511b-197">USA &quot; più breve &quot;  /  &quot; lo stesso &quot;  /  &quot; più a lungo&quot;</span><span class="sxs-lookup"><span data-stu-id="5511b-197">Uses &quot;Shorter&quot; / &quot;Same&quot; / &quot;Longer&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5511b-198">speed</span><span class="sxs-lookup"><span data-stu-id="5511b-198">Speed</span></span></td>
<td><span data-ttu-id="5511b-199">USA &quot; più lentamente &quot;  /  &quot; lo stesso &quot;  /  &quot; più velocemente&quot;</span><span class="sxs-lookup"><span data-stu-id="5511b-199">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5511b-200">Tariffa</span><span class="sxs-lookup"><span data-stu-id="5511b-200">Rate</span></span></td>
<td><span data-ttu-id="5511b-201">USA &quot; più lentamente &quot;  /  &quot; lo stesso &quot;  /  &quot; più velocemente&quot;</span><span class="sxs-lookup"><span data-stu-id="5511b-201">Uses &quot;Slower&quot; / &quot;Same&quot; / &quot;Faster&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5511b-202">Classificazione</span><span class="sxs-lookup"><span data-stu-id="5511b-202">Rating</span></span></td>
<td><span data-ttu-id="5511b-203">USA &quot; &quot;  /  &quot; lo stesso &quot;  /  &quot; livello più alto&quot;</span><span class="sxs-lookup"><span data-stu-id="5511b-203">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5511b-204">Priorità</span><span class="sxs-lookup"><span data-stu-id="5511b-204">Priority</span></span></td>
<td><span data-ttu-id="5511b-205">USA &quot; &quot;  /  &quot; lo stesso &quot;  /  &quot; livello più alto&quot;</span><span class="sxs-lookup"><span data-stu-id="5511b-205">Uses &quot;Lower&quot; / &quot;Same&quot; / &quot;Higher&quot;</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5511b-206">defaultSortDirection</span><span class="sxs-lookup"><span data-stu-id="5511b-206">defaultSortDirection</span></span></td>
<td><span data-ttu-id="5511b-207">Specifica la direzione di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="5511b-207">Specifies sort direction.</span></span> <span data-ttu-id="5511b-208">Il valore predefinito è &quot; Ascending &quot; .</span><span class="sxs-lookup"><span data-stu-id="5511b-208">Default is &quot;Ascending&quot;.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5511b-209">Valore</span><span class="sxs-lookup"><span data-stu-id="5511b-209">Value</span></span></th>
<th><span data-ttu-id="5511b-210">Significato</span><span class="sxs-lookup"><span data-stu-id="5511b-210">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5511b-211">Crescente</span><span class="sxs-lookup"><span data-stu-id="5511b-211">Ascending</span></span></td>
<td><span data-ttu-id="5511b-212">Ordinamento crescente.</span><span class="sxs-lookup"><span data-stu-id="5511b-212">Sorts ascending.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5511b-213">Decrescente</span><span class="sxs-lookup"><span data-stu-id="5511b-213">Descending</span></span></td>
<td><span data-ttu-id="5511b-214">Ordinamento decrescente.</span><span class="sxs-lookup"><span data-stu-id="5511b-214">Sorts descending.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
