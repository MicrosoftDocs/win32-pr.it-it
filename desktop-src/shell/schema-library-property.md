---
description: L' <property> elemento specifica una proprietà usata dalla libreria. Queste proprietà sono specifiche della libreria, quindi non esiste alcun set predefinito di nomi di proprietà da usare. Questo elemento è facoltativo e non ha elementi figlio.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Elemento Property (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b269e8914cf1f5da92d96e1922f7347a161daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993765"
---
# <a name="property-element-library-schema"></a><span data-ttu-id="8ad73-105">Elemento Property (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="8ad73-105">property Element (Library Schema)</span></span>

<span data-ttu-id="8ad73-106">L' <property> elemento specifica una proprietà usata dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="8ad73-106">The <property> element specifies a property used by the library.</span></span> <span data-ttu-id="8ad73-107">Queste proprietà sono specifiche della libreria, quindi non esiste alcun set predefinito di nomi di proprietà da usare.</span><span class="sxs-lookup"><span data-stu-id="8ad73-107">These properties are specific to the library, so there is no predefined set of property names to use.</span></span> <span data-ttu-id="8ad73-108">Questo elemento è facoltativo e non ha elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="8ad73-108">This element is optional and has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ad73-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ad73-109">Syntax</span></span>

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="8ad73-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8ad73-110">Element Information</span></span>



| <span data-ttu-id="8ad73-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="8ad73-111">Parent Element</span></span>                                                             | <span data-ttu-id="8ad73-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8ad73-112">Child Elements</span></span> |
|----------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="8ad73-113">Elemento propertyStore (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="8ad73-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) | <span data-ttu-id="8ad73-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="8ad73-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="8ad73-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="8ad73-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ad73-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="8ad73-116">Attribute</span></span></th>
<th><span data-ttu-id="8ad73-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ad73-117">Description</span></span></th>
<th><span data-ttu-id="8ad73-118">Valori</span><span class="sxs-lookup"><span data-stu-id="8ad73-118">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ad73-119">name</span><span class="sxs-lookup"><span data-stu-id="8ad73-119">name</span></span></td>
<td><span data-ttu-id="8ad73-120">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="8ad73-120">Public.</span></span> <span data-ttu-id="8ad73-121">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ad73-121">Required.</span></span> <span data-ttu-id="8ad73-122">Nome visualizzato della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8ad73-122">The display name of the property.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8ad73-123">tipo</span><span class="sxs-lookup"><span data-stu-id="8ad73-123">type</span></span></td>
<td><span data-ttu-id="8ad73-124">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="8ad73-124">Public.</span></span> <span data-ttu-id="8ad73-125">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ad73-125">Required.</span></span> <span data-ttu-id="8ad73-126">Tipo di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8ad73-126">The type of property.</span></span></td>
<td><ul>
<li><span data-ttu-id="8ad73-127">Any: valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="8ad73-127">Any: Default.</span></span> <span data-ttu-id="8ad73-128">Il valore non verrà forzato dal sottosistema di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8ad73-128">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="8ad73-129">VT_NULL verrà restituito da GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="8ad73-129">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="8ad73-130">Null: non è presente alcun valore per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8ad73-130">Null: There is no value for this property.</span></span> <span data-ttu-id="8ad73-131">VT_NULL verrà restituito da GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="8ad73-131">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="8ad73-132">Stringa: il valore deve essere un VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="8ad73-132">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="8ad73-133">Booleano: il valore deve essere un VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="8ad73-133">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="8ad73-134">Byte: il valore deve essere un VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="8ad73-134">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="8ad73-135">Buffer: il valore deve essere un VT_UI1 | VT_VECTOR buffer di byte.</span><span class="sxs-lookup"><span data-stu-id="8ad73-135">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="8ad73-136">Int16: il valore deve essere un VT_I2.</span><span class="sxs-lookup"><span data-stu-id="8ad73-136">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="8ad73-137">UInt16: il valore deve essere un VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="8ad73-137">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="8ad73-138">Int32: il valore deve essere un VT_I4.</span><span class="sxs-lookup"><span data-stu-id="8ad73-138">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="8ad73-139">UInt32: il valore deve essere un VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="8ad73-139">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="8ad73-140">Int64: il valore deve essere un VT_I8.</span><span class="sxs-lookup"><span data-stu-id="8ad73-140">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="8ad73-141">UInt64: il valore deve essere un VT_UI8.</span><span class="sxs-lookup"><span data-stu-id="8ad73-141">UInt64: The value must be a VT_UI8.</span></span></li>
<li><span data-ttu-id="8ad73-142">Double: il valore deve essere un VT_R8.</span><span class="sxs-lookup"><span data-stu-id="8ad73-142">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="8ad73-143">DateTime: il valore deve essere un VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="8ad73-143">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="8ad73-144">GUID: il valore deve essere un VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="8ad73-144">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="8ad73-145">BLOB: il valore deve essere un VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="8ad73-145">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="8ad73-146">Oggetto: il valore deve essere un VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="8ad73-146">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="8ad73-147">Stream: il valore deve essere un VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="8ad73-147">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="8ad73-148">Appunti: il valore deve essere un VT_CF.</span><span class="sxs-lookup"><span data-stu-id="8ad73-148">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8ad73-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ad73-149">Remarks</span></span>

<span data-ttu-id="8ad73-150">I requisiti per l'elemento> nome canonico <corrispondono ai requisiti per Windows Search e il sistema di proprietà di Windows.</span><span class="sxs-lookup"><span data-stu-id="8ad73-150">The requirements for the <canonical-name> element match the requirements for Windows Search and the Windows property system.</span></span> <span data-ttu-id="8ad73-151">La stringa deve essere di tipo canonico.</span><span class="sxs-lookup"><span data-stu-id="8ad73-151">The string must be of type canonical-type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ad73-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ad73-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ad73-153">Schema Descrizione libreria</span><span class="sxs-lookup"><span data-stu-id="8ad73-153">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="8ad73-154">Schemi proprietà</span><span class="sxs-lookup"><span data-stu-id="8ad73-154">Property Schemas</span></span>](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="8ad73-155">Cerca nello schema di descrizione del connettore</span><span class="sxs-lookup"><span data-stu-id="8ad73-155">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
