---
description: Specifica le informazioni sul tipo di una proprietà.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: typeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310108"
---
# <a name="typeinfo"></a><span data-ttu-id="ee49c-103">typeInfo</span><span class="sxs-lookup"><span data-stu-id="ee49c-103">typeInfo</span></span>

<span data-ttu-id="ee49c-104">Specifica le informazioni sul tipo di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee49c-104">Specifies a property's type information.</span></span> <span data-ttu-id="ee49c-105">Deve essere presente un solo elemento [TypeInfo]() per ogni [PropertyDescription](./propdesc-schema-propertydescription.md).</span><span class="sxs-lookup"><span data-stu-id="ee49c-105">There should be only one [typeInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md).</span></span> <span data-ttu-id="ee49c-106">Questo elemento è stato modificato per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ee49c-106">This element has changed for Windows 7.</span></span>

<span data-ttu-id="ee49c-107">Se sono presenti più elementi, viene usato l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="ee49c-108">Se non viene specificato alcun elemento [TypeInfo]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee49c-108">If no [typeInfo]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="ee49c-109">Sintassi per Windows 7</span><span class="sxs-lookup"><span data-stu-id="ee49c-109">Syntax for Windows 7</span></span>


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="ee49c-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ee49c-110">Element Information</span></span>



| <span data-ttu-id="ee49c-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="ee49c-111">Parent Element</span></span>                                                   | <span data-ttu-id="ee49c-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ee49c-112">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="ee49c-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="ee49c-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="ee49c-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="ee49c-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="ee49c-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="ee49c-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee49c-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="ee49c-116">Attribute</span></span></th>
<th><span data-ttu-id="ee49c-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee49c-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee49c-118">type</span><span class="sxs-lookup"><span data-stu-id="ee49c-118">type</span></span></td>
<td><span data-ttu-id="ee49c-119">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-119">Public.</span></span> <span data-ttu-id="ee49c-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-120">Optional.</span></span> <span data-ttu-id="ee49c-121">Il valore predefinito è &quot; Any &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-121">Default is &quot;Any&quot;.</span></span> <span data-ttu-id="ee49c-122">Indica il tipo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee49c-122">Indicates the type of the property.</span></span> <span data-ttu-id="ee49c-123">Di seguito sono riportati i tipi validi e i tipi Variant associati vengono recuperati da <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-123">The following are valid types and their associated variant types are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a>.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ee49c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ee49c-124">Value</span></span></th>
<th><span data-ttu-id="ee49c-125">Significato</span><span class="sxs-lookup"><span data-stu-id="ee49c-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee49c-126">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="ee49c-126">Any</span></span></td>
<td><span data-ttu-id="ee49c-127">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ee49c-127">Default.</span></span> <span data-ttu-id="ee49c-128">Il sottosistema di proprietà non impone né forza il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee49c-128">The property subsystem will not enforce or coerce the property value.</span></span> <span data-ttu-id="ee49c-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a> Restituisce VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="ee49c-129"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span> <span data-ttu-id="ee49c-130">I fornitori di software indipendenti (ISV) sono vivamente invitati a fornire un tipo anziché eseguire il fallback su questa impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ee49c-130">Independent software vendors (ISVs) are strongly encouraged to provide a type rather than fall back on this default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-131">Null</span><span class="sxs-lookup"><span data-stu-id="ee49c-131">Null</span></span></td>
<td><span data-ttu-id="ee49c-132">Non esiste alcun valore per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee49c-132">There is no value for this property.</span></span> <span data-ttu-id="ee49c-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a> Restituisce VT_NULL.</span><span class="sxs-lookup"><span data-stu-id="ee49c-133"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> returns VT_NULL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-134">string</span><span class="sxs-lookup"><span data-stu-id="ee49c-134">String</span></span></td>
<td><span data-ttu-id="ee49c-135">Il valore deve essere un VT_LPWSTR, ovvero una stringa Unicode terminata da un riferimento null.</span><span class="sxs-lookup"><span data-stu-id="ee49c-135">The value must be a VT_LPWSTR, which is a Unicode string terminated by a null reference.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee49c-136">Boolean</span></span></td>
<td><span data-ttu-id="ee49c-137">Il valore deve essere un VT_BOOL, ovvero un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="ee49c-137">The value must be a VT_BOOL, which is a boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-138">Byte</span><span class="sxs-lookup"><span data-stu-id="ee49c-138">Byte</span></span></td>
<td><span data-ttu-id="ee49c-139">Il valore deve essere un VT_UI1, che è un byte.</span><span class="sxs-lookup"><span data-stu-id="ee49c-139">The value must be a VT_UI1, which is a byte.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-140">Buffer</span><span class="sxs-lookup"><span data-stu-id="ee49c-140">Buffer</span></span></td>
<td><span data-ttu-id="ee49c-141">Il valore deve essere un VT_UI1 | VT_VECTOR buffer di byte.</span><span class="sxs-lookup"><span data-stu-id="ee49c-141">The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-142">Int16</span><span class="sxs-lookup"><span data-stu-id="ee49c-142">Int16</span></span></td>
<td><span data-ttu-id="ee49c-143">Il valore deve essere un VT_I2, ovvero un Integer a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="ee49c-143">The value must be a VT_I2, which is a 16-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-144">UInt16</span><span class="sxs-lookup"><span data-stu-id="ee49c-144">UInt16</span></span></td>
<td><span data-ttu-id="ee49c-145">Il valore deve essere un VT_UI2, ovvero una Unsigned Integer a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="ee49c-145">The value must be a VT_UI2, which is a 16-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-146">Int32</span><span class="sxs-lookup"><span data-stu-id="ee49c-146">Int32</span></span></td>
<td><span data-ttu-id="ee49c-147">Il valore deve essere un VT_I4, ovvero un intero a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ee49c-147">The value must be a VT_I4, which is a 32-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-148">UInt32</span><span class="sxs-lookup"><span data-stu-id="ee49c-148">UInt32</span></span></td>
<td><span data-ttu-id="ee49c-149">Il valore deve essere un VT_UI4, ovvero una Unsigned Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ee49c-149">The value must be a VT_UI4, which is a 32-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-150">Int64</span><span class="sxs-lookup"><span data-stu-id="ee49c-150">Int64</span></span></td>
<td><span data-ttu-id="ee49c-151">Il valore deve essere un VT_I8, ovvero un intero a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ee49c-151">The value must be a VT_I8, which is a 64-bit integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-152">UInt64</span><span class="sxs-lookup"><span data-stu-id="ee49c-152">UInt64</span></span></td>
<td><span data-ttu-id="ee49c-153">Il valore deve essere un VT_UI8, ovvero una Unsigned Integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ee49c-153">The value must be a VT_UI8, which is a 64-bit unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-154">Double</span><span class="sxs-lookup"><span data-stu-id="ee49c-154">Double</span></span></td>
<td><span data-ttu-id="ee49c-155">Il valore deve essere un VT_R8, che è un valore Double.</span><span class="sxs-lookup"><span data-stu-id="ee49c-155">The value must be a VT_R8, which is a double.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-156">Datetime</span><span class="sxs-lookup"><span data-stu-id="ee49c-156">DateTime</span></span></td>
<td><span data-ttu-id="ee49c-157">Il valore deve essere un VT_FILETIME, che è un <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-157">The value must be a VT_FILETIME, which is a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-158">Guid</span><span class="sxs-lookup"><span data-stu-id="ee49c-158">Guid</span></span></td>
<td><span data-ttu-id="ee49c-159">Il valore deve essere un VT_CLSID, ovvero un identificatore di classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="ee49c-159">The value must be a VT_CLSID, which is a class identifier (CLSID).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-160">BLOB</span><span class="sxs-lookup"><span data-stu-id="ee49c-160">Blob</span></span></td>
<td><span data-ttu-id="ee49c-161">Il valore deve essere un VT_BLOB, ovvero byte con prefisso di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="ee49c-161">The value must be a VT_BLOB, which are length-prefixed bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-162">Stream</span><span class="sxs-lookup"><span data-stu-id="ee49c-162">Stream</span></span></td>
<td><span data-ttu-id="ee49c-163">Il valore deve essere un VT_STREAM, ovvero un oggetto che implementa <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-163">The value must be a VT_STREAM, which is an object that implements <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-164">Appunti</span><span class="sxs-lookup"><span data-stu-id="ee49c-164">Clipboard</span></span></td>
<td><span data-ttu-id="ee49c-165">Il valore deve essere un VT_CF, che è un formato degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="ee49c-165">The value must be a VT_CF, which is a clipboard format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-166">Oggetto</span><span class="sxs-lookup"><span data-stu-id="ee49c-166">Object</span></span></td>
<td><span data-ttu-id="ee49c-167">Il valore deve essere un VT_UNKNOWN, ovvero un oggetto che implementa <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-167">The value must be a VT_UNKNOWN, which is an object that implements <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-168">groupingRange</span><span class="sxs-lookup"><span data-stu-id="ee49c-168">groupingRange</span></span></td>
<td><span data-ttu-id="ee49c-169">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-169">Optional.</span></span> <span data-ttu-id="ee49c-170">Il valore predefinito è &quot; discreto &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-170">Default is &quot;Discrete&quot;.</span></span> <span data-ttu-id="ee49c-171">Specifica la modalità di visualizzazione della proprietà quando una visualizzazione viene raggruppata in base a questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee49c-171">Specifies how the property is displayed when a view is grouped by this property.</span></span> <span data-ttu-id="ee49c-172">Una volta impostati qui, questi valori vengono recuperati da <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription:: GetGroupingRange</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-172">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription::GetGroupingRange</strong></a>.</span></span> <span data-ttu-id="ee49c-173">Di seguito sono riportati i tipi validi.</span><span class="sxs-lookup"><span data-stu-id="ee49c-173">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ee49c-174">Valore</span><span class="sxs-lookup"><span data-stu-id="ee49c-174">Value</span></span></th>
<th><span data-ttu-id="ee49c-175">Significato</span><span class="sxs-lookup"><span data-stu-id="ee49c-175">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee49c-176">Discrete</span><span class="sxs-lookup"><span data-stu-id="ee49c-176">Discrete</span></span></td>
<td><span data-ttu-id="ee49c-177">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ee49c-177">Default.</span></span> <span data-ttu-id="ee49c-178">Visualizza i singoli valori.</span><span class="sxs-lookup"><span data-stu-id="ee49c-178">Displays individual values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-179">Alfanumerico</span><span class="sxs-lookup"><span data-stu-id="ee49c-179">Alphanumeric</span></span></td>
<td><span data-ttu-id="ee49c-180">Visualizza gli intervalli alfanumerici statici per i valori.</span><span class="sxs-lookup"><span data-stu-id="ee49c-180">Displays static alphanumeric ranges for values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-181">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ee49c-181">Size</span></span></td>
<td><span data-ttu-id="ee49c-182">Visualizza gli intervalli di dimensioni statiche per i valori.</span><span class="sxs-lookup"><span data-stu-id="ee49c-182">Displays static size ranges for values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-183">Data</span><span class="sxs-lookup"><span data-stu-id="ee49c-183">Date</span></span></td>
<td><span data-ttu-id="ee49c-184">Visualizza i gruppi mese/anno.</span><span class="sxs-lookup"><span data-stu-id="ee49c-184">Displays month/year groups.</span></span> <span data-ttu-id="ee49c-185">Valore predefinito per le proprietà di tipo = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-185">Default for properties of type=&quot;DateTime&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-186">TimeRelative</span><span class="sxs-lookup"><span data-stu-id="ee49c-186">TimeRelative</span></span></td>
<td><span data-ttu-id="ee49c-187">Viene visualizzato nei gruppi relativi al tempo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-187">Displays in time-relative groups.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-188">Dynamic</span><span class="sxs-lookup"><span data-stu-id="ee49c-188">Dynamic</span></span></td>
<td><span data-ttu-id="ee49c-189">Visualizza gli intervalli creati dinamicamente per i valori.</span><span class="sxs-lookup"><span data-stu-id="ee49c-189">Displays dynamically created ranges for the values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-190">Percentuale</span><span class="sxs-lookup"><span data-stu-id="ee49c-190">Percent</span></span></td>
<td><span data-ttu-id="ee49c-191">Visualizza i bucket percentuali.</span><span class="sxs-lookup"><span data-stu-id="ee49c-191">Displays percent buckets.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-192">innata</span><span class="sxs-lookup"><span data-stu-id="ee49c-192">isInnate</span></span></td>
<td><span data-ttu-id="ee49c-193">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-193">Public.</span></span> <span data-ttu-id="ee49c-194">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-194">Optional.</span></span> <span data-ttu-id="ee49c-195">Il valore predefinito è &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ee49c-195">Default is &quot;false&quot;.</span></span> <span data-ttu-id="ee49c-196">Specifica se la proprietà è considerata innata.</span><span class="sxs-lookup"><span data-stu-id="ee49c-196">Specifies whether the property is considered innate.</span></span> <span data-ttu-id="ee49c-197">Una proprietà innata è una proprietà calcolata dal contenuto di un file o da altri sistemi o risorse.</span><span class="sxs-lookup"><span data-stu-id="ee49c-197">An innate property is one which is either calculated from the content of a file, or from other resources or systems.</span></span> <span data-ttu-id="ee49c-198">System. size, ad esempio, è una proprietà innata fornita dal file system; la modifica del valore della proprietà in e di per sé non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="ee49c-198">For example, System.Size is an innate property provided by the file system; changing the value of the property in and of itself does nothing.</span></span> <span data-ttu-id="ee49c-199">Altri esempi sono System. image. Dimensions e System.Document. PageCount, che vengono calcolate da programmi basati sul contenuto del file, non in base a un'impostazione modificabile dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ee49c-199">Other examples are System.Image.Dimensions and System.Document.PageCount, which are calculated by programs based upon the content of the file, not based upon a user-changeable setting.</span></span> <span data-ttu-id="ee49c-200">L'impostazione di innate = &quot; true &quot; indica che l'utente non può modificare direttamente questa proprietà tramite un controllo proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee49c-200">Setting isInnate=&quot;true&quot; means the user cannot edit this property directly via a property control.</span></span> <span data-ttu-id="ee49c-201">Questo valore esegue il mapping al flag di PDTF_ISINNATE definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-201">This value maps to the PDTF_ISINNATE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-202">canBePurged</span><span class="sxs-lookup"><span data-stu-id="ee49c-202">canBePurged</span></span></td>
<td><span data-ttu-id="ee49c-203"><strong>Windows Vista con Service Pack 1 (SP1) e versioni successive</strong>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-203"><strong>Windows Vista with Service Pack 1 (SP1) and later only</strong>.</span></span> <span data-ttu-id="ee49c-204">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-204">Public.</span></span> <span data-ttu-id="ee49c-205">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-205">Optional.</span></span> <span data-ttu-id="ee49c-206">Se impostato su &quot; true &quot; , consente di eliminare una proprietà innata.</span><span class="sxs-lookup"><span data-stu-id="ee49c-206">When set to &quot;true&quot;, allows an innate property to be deleted.</span></span> <span data-ttu-id="ee49c-207">Le proprietà innate, che vengono calcolate da altre proprietà, sono di sola lettura per definizione.</span><span class="sxs-lookup"><span data-stu-id="ee49c-207">Innate properties, which are calculated from other properties, are read-only by definition.</span></span> <span data-ttu-id="ee49c-208">Il valore predefinito di questo attributo dipende dal valore di <em>innate</em> .</span><span class="sxs-lookup"><span data-stu-id="ee49c-208">The default value for this attribute depends on the <em>isInnate</em> value.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ee49c-209">innata</span><span class="sxs-lookup"><span data-stu-id="ee49c-209">isInnate</span></span></th>
<th><span data-ttu-id="ee49c-210">Valore predefinito di canBePurged</span><span class="sxs-lookup"><span data-stu-id="ee49c-210">canBePurged Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee49c-211">true</span><span class="sxs-lookup"><span data-stu-id="ee49c-211">true</span></span></td>
<td><span data-ttu-id="ee49c-212">false</span><span class="sxs-lookup"><span data-stu-id="ee49c-212">false</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-213">false</span><span class="sxs-lookup"><span data-stu-id="ee49c-213">false</span></span></td>
<td><span data-ttu-id="ee49c-214">true</span><span class="sxs-lookup"><span data-stu-id="ee49c-214">true</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="ee49c-215">Una proprietà il cui valore <em>innate</em> è &quot; false &quot; (ovvero la proprietà è di lettura/scrittura) non può inoltre impostare il valore <em>canBePurged</em> su &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-215">A property whose <em>isInnate</em> value is &quot;false&quot; (meaning that the property is read/write) cannot also set the <em>canBePurged</em> value to &quot;false&quot;.</span></span> <span data-ttu-id="ee49c-216">Questa restrizione viene applicata dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-216">This restriction is enforced by the operating system.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="ee49c-217">Anche se questo attributo è stato introdotto in Windows Vista con Service Pack 1 (SP1), un file con estensione propdesc che include questo attributo è compatibile con Windows Vista prima di Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="ee49c-217">Although this attribute was introduced in Windows Vista with Service Pack 1 (SP1), a .propdesc file that includes this attribute is compatible with Windows Vista prior to Windows Vista with SP1.</span></span> <span data-ttu-id="ee49c-218">In questa situazione, l'attributo <em>canBePurged</em> viene semplicemente ignorato.</span><span class="sxs-lookup"><span data-stu-id="ee49c-218">The <em>canBePurged</em> attribute is simply ignored in that situation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-219">multipleValues</span><span class="sxs-lookup"><span data-stu-id="ee49c-219">multipleValues</span></span></td>
<td><span data-ttu-id="ee49c-220">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-220">Public.</span></span> <span data-ttu-id="ee49c-221">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-221">Optional.</span></span> <span data-ttu-id="ee49c-222">Il valore predefinito è &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ee49c-222">Default is &quot;false&quot;.</span></span> <span data-ttu-id="ee49c-223">Specifica se la proprietà può avere più valori.</span><span class="sxs-lookup"><span data-stu-id="ee49c-223">Specifies whether this property can have multiple values.</span></span> <span data-ttu-id="ee49c-224">Questo valore esegue il mapping al flag di PDTF_MULTIPLEVALUES definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-224">This value maps to the PDTF_MULTIPLEVALUES flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span> <span data-ttu-id="ee49c-225">Ciò influisce anche sul fatto che VT_VECTOR sia o a un VARTYPE del valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee49c-225">This also influences whether VT_VECTOR is OR'd to the VARTYPE of the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-226">isGroup</span><span class="sxs-lookup"><span data-stu-id="ee49c-226">isGroup</span></span></td>
<td><span data-ttu-id="ee49c-227">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-227">Public.</span></span> <span data-ttu-id="ee49c-228">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-228">Optional.</span></span> <span data-ttu-id="ee49c-229">Il valore predefinito è &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ee49c-229">Default is &quot;false&quot;.</span></span> <span data-ttu-id="ee49c-230">Specifica se la proprietà è un'intestazione di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-230">Specifies whether the property is a group heading.</span></span> <span data-ttu-id="ee49c-231">Un'intestazione di gruppo viene utilizzata rigorosamente in proplists, non ha alcun valore, non viene mai archiviata in un file e deve avere anche <typeInfo type=&quot;Null&quot;> .</span><span class="sxs-lookup"><span data-stu-id="ee49c-231">A group heading is strictly used in proplists, has no value, is never stored in a file, and should also have <typeInfo type=&quot;Null&quot;>.</span></span> <span data-ttu-id="ee49c-232">Alcune interfacce utente del sistema usano proplists per indicare la sequenza delle proprietà da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="ee49c-232">Some UI in the system use proplists to indicate the sequence of the properties to display.</span></span> <span data-ttu-id="ee49c-233">Questi proplists possono includere riferimenti a intestazioni di gruppo (ad esempio, System. PropGroup. camera), che indicano all'interfaccia utente di avviare una nuova sezione del gruppo (ad esempio, &quot; le impostazioni della fotocamera &quot; ).</span><span class="sxs-lookup"><span data-stu-id="ee49c-233">These proplists may include references to group headings (eg, System.PropGroup.Camera), which tell the UI to start a new group section (eg, &quot;Camera Settings&quot;).</span></span> <span data-ttu-id="ee49c-234">Una descrizione della proprietà con il valore di ' Group = &quot; true &quot; ' deve specificare un oggetto <labelInfo label=&quot;Some localized label&quot;> ; in caso contrario, non è una proprietà utile.</span><span class="sxs-lookup"><span data-stu-id="ee49c-234">A property description with isGroup=&quot;true&quot; should specify a <labelInfo label=&quot;Some localized label&quot;>, otherwise it isn't a useful property.</span></span> <span data-ttu-id="ee49c-235">Questo valore esegue il mapping al flag di PDTF_ISGROUP definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-235">This value maps to the PDTF_ISGROUP flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-236">aggregationType</span><span class="sxs-lookup"><span data-stu-id="ee49c-236">aggregationType</span></span></td>
<td><span data-ttu-id="ee49c-237">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-237">Public.</span></span> <span data-ttu-id="ee49c-238">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-238">Optional.</span></span> <span data-ttu-id="ee49c-239">Il valore predefinito è &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-239">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="ee49c-240">Specifica la modalità di visualizzazione delle proprietà di aggregazione quando vengono selezionati più elementi.</span><span class="sxs-lookup"><span data-stu-id="ee49c-240">Specifies how aggregate properties are displayed when multiple items are selected.</span></span> <span data-ttu-id="ee49c-241">Una volta impostati qui, questi valori vengono recuperati da <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription:: GetAggregationType</strong></a> come <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-241">Once set here, these values are retrieved by <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription::GetAggregationType</strong></a> as an <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>.</span></span> <span data-ttu-id="ee49c-242">Di seguito sono riportati i tipi validi.</span><span class="sxs-lookup"><span data-stu-id="ee49c-242">The following are valid types.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ee49c-243">Valore</span><span class="sxs-lookup"><span data-stu-id="ee49c-243">Value</span></span></th>
<th><span data-ttu-id="ee49c-244">Significato</span><span class="sxs-lookup"><span data-stu-id="ee49c-244">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee49c-245">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee49c-245">Default</span></span></td>
<td><span data-ttu-id="ee49c-246">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ee49c-246">Default.</span></span> <span data-ttu-id="ee49c-247">Visualizza un segnaposto con <strong>più valori</strong> nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ee49c-247">Displays a <strong>Multiple Values</strong> placeholder in the UI.</span></span> <span data-ttu-id="ee49c-248">Si tratta dell'impostazione predefinita se il <em>tipo</em> non è compatibile con il <em>aggregationType</em>specificato.</span><span class="sxs-lookup"><span data-stu-id="ee49c-248">This is the default if the <em>type</em> is incompatible with the specified <em>aggregationType</em>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-249">First (Primo)</span><span class="sxs-lookup"><span data-stu-id="ee49c-249">First</span></span></td>
<td><span data-ttu-id="ee49c-250">Consente di visualizzare il valore della proprietà del primo elemento della selezione o della raccolta.</span><span class="sxs-lookup"><span data-stu-id="ee49c-250">Displays the property value of the first item in the selection or collection.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-251">Sum</span><span class="sxs-lookup"><span data-stu-id="ee49c-251">Sum</span></span></td>
<td><span data-ttu-id="ee49c-252">Visualizza la somma dei valori numerici.</span><span class="sxs-lookup"><span data-stu-id="ee49c-252">Displays the sum of the numerical values.</span></span> <span data-ttu-id="ee49c-253">Utile per proprietà quali System. Media. Duration o System. size.</span><span class="sxs-lookup"><span data-stu-id="ee49c-253">Useful for properties such as System.Media.Duration or System.Size.</span></span> <span data-ttu-id="ee49c-254">Questo valore non è compatibile con i tipi non numerici.</span><span class="sxs-lookup"><span data-stu-id="ee49c-254">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-255">Media</span><span class="sxs-lookup"><span data-stu-id="ee49c-255">Average</span></span></td>
<td><span data-ttu-id="ee49c-256">Visualizza la media dei valori numerici.</span><span class="sxs-lookup"><span data-stu-id="ee49c-256">Displays the average of the numerical values.</span></span> <span data-ttu-id="ee49c-257">Utile per proprietà quali System. rating.</span><span class="sxs-lookup"><span data-stu-id="ee49c-257">Useful for properties such as System.Rating.</span></span> <span data-ttu-id="ee49c-258">Questo valore non è compatibile con i tipi non numerici.</span><span class="sxs-lookup"><span data-stu-id="ee49c-258">This value is not compatible with non-numeric types.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-259">DateRange</span><span class="sxs-lookup"><span data-stu-id="ee49c-259">DateRange</span></span></td>
<td><span data-ttu-id="ee49c-260">Visualizza un intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="ee49c-260">Displays a range of dates.</span></span> <span data-ttu-id="ee49c-261">Utile per proprietà quali System. Photo. DateTaken.</span><span class="sxs-lookup"><span data-stu-id="ee49c-261">Useful for properties like System.Photo.DateTaken.</span></span> <span data-ttu-id="ee49c-262">Questo valore non è compatibile con qualsiasi elemento tranne Type = &quot; DateTime &quot; ed è il valore predefinito per le proprietà di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-262">This value is not compatible with anything except type=&quot;DateTime&quot; and is the default for properties of that type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-263">Union</span><span class="sxs-lookup"><span data-stu-id="ee49c-263">Union</span></span></td>
<td><span data-ttu-id="ee49c-264">Consente di visualizzare un'Unione di tutti i valori della selezione o della raccolta.</span><span class="sxs-lookup"><span data-stu-id="ee49c-264">Displays a union of all the values in the selection or collection.</span></span> <span data-ttu-id="ee49c-265">L'ordine in cui vengono visualizzati i valori non è definito.</span><span class="sxs-lookup"><span data-stu-id="ee49c-265">The order in which the values are shown is undefined.</span></span> <span data-ttu-id="ee49c-266">Questo valore è l'impostazione predefinita per le proprietà di tipo = &quot; String &quot; e multipleValues = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-266">This value is the default for properties of type=&quot;String&quot; and multipleValues=&quot;true&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-267">Massimo</span><span class="sxs-lookup"><span data-stu-id="ee49c-267">Maximum</span></span></td>
<td><span data-ttu-id="ee49c-268">Consente di visualizzare il valore massimo nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="ee49c-268">Displays the maximum value in the collection.</span></span> <span data-ttu-id="ee49c-269">Utile per proprietà quali System. DateModified.</span><span class="sxs-lookup"><span data-stu-id="ee49c-269">Useful for properties like System.DateModified.</span></span> <span data-ttu-id="ee49c-270">Non è compatibile con i tipi non numerici o non di data.</span><span class="sxs-lookup"><span data-stu-id="ee49c-270">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-271">Minima</span><span class="sxs-lookup"><span data-stu-id="ee49c-271">Minimum</span></span></td>
<td><span data-ttu-id="ee49c-272">Consente di visualizzare il valore minimo nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="ee49c-272">Displays the minimum value in the collection.</span></span> <span data-ttu-id="ee49c-273">Non è compatibile con i tipi non numerici o non di data.</span><span class="sxs-lookup"><span data-stu-id="ee49c-273">Not compatible with non-numeric or non-date types.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-274">isTreeProperty</span><span class="sxs-lookup"><span data-stu-id="ee49c-274">isTreeProperty</span></span></td>
<td><span data-ttu-id="ee49c-275">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-275">Public.</span></span> <span data-ttu-id="ee49c-276">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-276">Optional.</span></span> <span data-ttu-id="ee49c-277">Il valore predefinito è &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ee49c-277">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-278">Visualizzabile</span><span class="sxs-lookup"><span data-stu-id="ee49c-278">isViewable</span></span></td>
<td><span data-ttu-id="ee49c-279">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-279">Public.</span></span> <span data-ttu-id="ee49c-280">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-280">Optional.</span></span> <span data-ttu-id="ee49c-281">Il valore predefinito è &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ee49c-281">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="ee49c-282">Specifica se questa proprietà deve essere visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="ee49c-282">Specifies whether this property is intended to be viewable to the user.</span></span> <span data-ttu-id="ee49c-283">Ad esempio, l'interfaccia utente di selezione colonne Mostra solo le proprietà con l'oggetto visualizzabile = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-283">For example, the Column Chooser UI only shows the properties that have isViewable=&quot;true&quot;.</span></span> <span data-ttu-id="ee49c-284">L'eccezione è l'interfaccia utente basata su un oggetto prop, che Mostra sempre la proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee49c-284">The exception is UI that is driven by a proplist, which will always show the property.</span></span> <span data-ttu-id="ee49c-285">Se si dispone di una proprietà che è destinata solo a eseguire la spola dei dati tra due oggetti e non è mai stata progettata per essere visualizzata dall'utente, questo attributo deve essere false.</span><span class="sxs-lookup"><span data-stu-id="ee49c-285">If you have a property that is only meant to shuttle data between two objects, and never intended to be viewed by the user, this attribute should be false.</span></span> <span data-ttu-id="ee49c-286">Questo valore esegue il mapping al flag di PDTF_ISVIEWABLE definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-286">This value maps to the PDTF_ISVIEWABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-287">Queryable</span><span class="sxs-lookup"><span data-stu-id="ee49c-287">isQueryable</span></span></td>
<td><span data-ttu-id="ee49c-288">Solo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ee49c-288">Windows Vista only.</span></span> <span data-ttu-id="ee49c-289">Non supportato in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ee49c-289">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="ee49c-290">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-290">Public.</span></span> <span data-ttu-id="ee49c-291">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-291">Optional.</span></span> <span data-ttu-id="ee49c-292">Il valore predefinito è &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ee49c-292">Default value is &quot;false&quot;.</span></span> <span data-ttu-id="ee49c-293">Specifica se questa proprietà deve essere disponibile nell'interfaccia utente di ricerca Generatore di query.</span><span class="sxs-lookup"><span data-stu-id="ee49c-293">Specifies whether this property is intended to be available in the Search Query Builder UI.</span></span> <span data-ttu-id="ee49c-294">Una proprietà deve avere un valore di visualizzabile = &quot; true &quot; prima che &quot; venga rispettata l'esecuzione di Queryable = true &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-294">A property must have isViewable=&quot;true&quot; before isQueryable=&quot;true&quot; is respected.</span></span> <span data-ttu-id="ee49c-295">Questo valore esegue il mapping al flag di PDTF_ISQUERYABLE definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ee49c-295">This value maps to the PDTF_ISQUERYABLE flag defined in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> and used in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-296">searchRawValue</span><span class="sxs-lookup"><span data-stu-id="ee49c-296">searchRawValue</span></span></td>
<td><span data-ttu-id="ee49c-297"><strong>Windows 7 e versioni successive.</strong></span><span class="sxs-lookup"><span data-stu-id="ee49c-297"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="ee49c-298">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-298">Public.</span></span> <span data-ttu-id="ee49c-299">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-299">Optional.</span></span> <span data-ttu-id="ee49c-300">Il valore predefinito è &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ee49c-300">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-301">includeInFullTextQuery</span><span class="sxs-lookup"><span data-stu-id="ee49c-301">includeInFullTextQuery</span></span></td>
<td><span data-ttu-id="ee49c-302">Solo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ee49c-302">Windows Vista only.</span></span> <span data-ttu-id="ee49c-303">Non supportato in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ee49c-303">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="ee49c-304">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-304">Public.</span></span> <span data-ttu-id="ee49c-305">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-305">Optional.</span></span> <span data-ttu-id="ee49c-306">Il valore predefinito è &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="ee49c-306">Default value is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-307">conditionType</span><span class="sxs-lookup"><span data-stu-id="ee49c-307">conditionType</span></span></td>
<td><span data-ttu-id="ee49c-308">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-308">Public.</span></span> <span data-ttu-id="ee49c-309">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-309">Optional.</span></span> <span data-ttu-id="ee49c-310">Il valore predefinito è &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-310">Default is &quot;String&quot;.</span></span> <span data-ttu-id="ee49c-311">Specifica un hint per l'interfaccia utente di ricerca Generatore di query in modo che sia in grado di determinare l'elenco di possibili operatori di condizione all'interno di un predicato.</span><span class="sxs-lookup"><span data-stu-id="ee49c-311">Specifies a hint to the Search Query Builder UI so that it can determine the list of possible condition operators inside a predicate.</span></span> <span data-ttu-id="ee49c-312">Di seguito sono riportati i valori riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="ee49c-312">The following are recognized values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ee49c-313">Valore</span><span class="sxs-lookup"><span data-stu-id="ee49c-313">Value</span></span></th>
<th><span data-ttu-id="ee49c-314">Significato</span><span class="sxs-lookup"><span data-stu-id="ee49c-314">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee49c-315">string</span><span class="sxs-lookup"><span data-stu-id="ee49c-315">String</span></span></td>
<td><span data-ttu-id="ee49c-316">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ee49c-316">Default.</span></span> <span data-ttu-id="ee49c-317">Verranno utilizzati gli operatori seguenti: &quot; è &quot; , non è,,,, &quot; &quot; &quot; &lt; &quot; &quot; &gt; &quot; &quot; <= &quot; &quot; >= &quot; , &quot; inizia con &quot; , &quot; termina con &quot; , &quot; Contains &quot; , &quot; non contiene &quot; , &quot; è simile a &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-317">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;&lt;&quot;, &quot;&gt;&quot;, &quot;<=&quot;, &quot;>=&quot;, &quot;starts with&quot;, &quot;ends with&quot;, &quot;contains&quot;, &quot;doesn't contain&quot;, &quot;is like&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-318">Number</span><span class="sxs-lookup"><span data-stu-id="ee49c-318">Number</span></span></td>
<td><span data-ttu-id="ee49c-319">Valore predefinito per le proprietà numeriche.</span><span class="sxs-lookup"><span data-stu-id="ee49c-319">Default for numeric properties.</span></span> <span data-ttu-id="ee49c-320">Verranno utilizzati gli operatori seguenti: &quot; uguale a, &quot; non uguale a, &quot; &quot; &quot; è minore di &quot; , &quot; è maggiore di &quot; , &quot; è minore o uguale a &quot; , &quot; è maggiore o uguale a &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-320">The following operators will be used: &quot;equals&quot;, &quot;doesn't equal&quot;, &quot;is less than&quot;, &quot;is greater than&quot;, &quot;is less than or equal to&quot;, &quot;is greater than or equal to&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-321">Datetime</span><span class="sxs-lookup"><span data-stu-id="ee49c-321">DateTime</span></span></td>
<td><span data-ttu-id="ee49c-322">Valore predefinito per le proprietà di tipo = &quot; DateTime &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-322">Default for properties of type=&quot;DateTime&quot;.</span></span> <span data-ttu-id="ee49c-323">Verranno utilizzati gli operatori seguenti: &quot; is &quot; , is &quot; Not &quot; , &quot; is before, is &quot; &quot; after &quot; , &quot; is before ma includes &quot; , is &quot; after ma includes &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-323">The following operators will be used: &quot;is&quot;, &quot;is not&quot;, &quot;is before&quot;, &quot;is after&quot;, &quot;is before but includes&quot;, &quot;is after but includes&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-324">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee49c-324">Boolean</span></span></td>
<td><span data-ttu-id="ee49c-325">Valore predefinito per le proprietà di tipo = &quot; Boolean &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-325">Default for properties of type=&quot;Boolean&quot;.</span></span> <span data-ttu-id="ee49c-326">Uguale al numero.</span><span class="sxs-lookup"><span data-stu-id="ee49c-326">Same as Number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-327">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ee49c-327">Size</span></span></td>
<td><span data-ttu-id="ee49c-328">Uguale al numero.</span><span class="sxs-lookup"><span data-stu-id="ee49c-328">Same as Number.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-329">defaultOperation</span><span class="sxs-lookup"><span data-stu-id="ee49c-329">defaultOperation</span></span></td>
<td><span data-ttu-id="ee49c-330">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="ee49c-330">Public.</span></span> <span data-ttu-id="ee49c-331">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ee49c-331">Optional.</span></span> <span data-ttu-id="ee49c-332">Il valore predefinito è &quot; uguale a &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-332">Default is &quot;Equal&quot;.</span></span> <span data-ttu-id="ee49c-333">Specifica un hint per lo strumento Generatore di query di ricerca in modo che sia in grado di determinare l'operatore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ee49c-333">Specifies a hint to the Search Query Builder tool so that it can determine the default operator.</span></span> <span data-ttu-id="ee49c-334">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee49c-334">The possible values are as follows:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ee49c-335">valore</span><span class="sxs-lookup"><span data-stu-id="ee49c-335">Value</span></span></th>
<th><span data-ttu-id="ee49c-336">Significato</span><span class="sxs-lookup"><span data-stu-id="ee49c-336">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee49c-337">Uguale a</span><span class="sxs-lookup"><span data-stu-id="ee49c-337">Equal</span></span></td>
<td><span data-ttu-id="ee49c-338">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ee49c-338">Default.</span></span> <span data-ttu-id="ee49c-339">Indica l'equivalente.</span><span class="sxs-lookup"><span data-stu-id="ee49c-339">Indicates equivalent.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-340">NotEqual</span><span class="sxs-lookup"><span data-stu-id="ee49c-340">NotEqual</span></span></td>
<td><span data-ttu-id="ee49c-341">Indica un valore diverso da.</span><span class="sxs-lookup"><span data-stu-id="ee49c-341">Indicates not equivalent.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-342">LessThan</span><span class="sxs-lookup"><span data-stu-id="ee49c-342">LessThan</span></span></td>
<td><span data-ttu-id="ee49c-343">Indica minore di.</span><span class="sxs-lookup"><span data-stu-id="ee49c-343">Indicates less than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee49c-344">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="ee49c-344">GreaterThan</span></span></td>
<td><span data-ttu-id="ee49c-345">Impostazione predefinita per le proprietà di conditionType = &quot; size &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-345">Default for properties of conditionType=&quot;Size&quot;.</span></span> <span data-ttu-id="ee49c-346">Indica maggiore di.</span><span class="sxs-lookup"><span data-stu-id="ee49c-346">Indicates greater than.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee49c-347">Contiene</span><span class="sxs-lookup"><span data-stu-id="ee49c-347">Contains</span></span></td>
<td><span data-ttu-id="ee49c-348">Impostazione predefinita per le proprietà di conditionType = &quot; String &quot; .</span><span class="sxs-lookup"><span data-stu-id="ee49c-348">Default for properties of conditionType=&quot;String&quot;.</span></span> <span data-ttu-id="ee49c-349">Indica l'inclusione.</span><span class="sxs-lookup"><span data-stu-id="ee49c-349">Indicates inclusion.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
