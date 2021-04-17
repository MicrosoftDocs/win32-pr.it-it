---
description: L' <property> elemento facoltativo specifica una proprietà usata dal connettore di ricerca. Queste proprietà sono specifiche di questo connettore di ricerca, pertanto non esiste alcun set predefinito di nomi da usare. Questo elemento non ha elementi figlio.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Elemento Property di propertyStore (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525452"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a><span data-ttu-id="cedfa-105">Elemento Property di propertyStore (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="cedfa-105">property Element of propertyStore (Search Connector Schema)</span></span>

<span data-ttu-id="cedfa-106">L' <property> elemento facoltativo specifica una proprietà usata dal connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="cedfa-106">The optional <property> element specifies a property used by the search connector.</span></span> <span data-ttu-id="cedfa-107">Queste proprietà sono specifiche di questo connettore di ricerca, pertanto non esiste alcun set predefinito di nomi da usare.</span><span class="sxs-lookup"><span data-stu-id="cedfa-107">These properties are specific to this search connector, so there is no predefined set of names to use.</span></span> <span data-ttu-id="cedfa-108">Questo elemento non ha elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="cedfa-108">This element has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="cedfa-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cedfa-109">Syntax</span></span>


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="cedfa-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cedfa-110">Element Information</span></span>



| <span data-ttu-id="cedfa-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="cedfa-111">Parent Element</span></span>                                                                           | <span data-ttu-id="cedfa-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="cedfa-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="cedfa-113">Elemento propertyStore (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="cedfa-113">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a><span data-ttu-id="cedfa-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="cedfa-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cedfa-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="cedfa-115">Attribute</span></span></th>
<th><span data-ttu-id="cedfa-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cedfa-116">Description</span></span></th>
<th><span data-ttu-id="cedfa-117">Valori</span><span class="sxs-lookup"><span data-stu-id="cedfa-117">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cedfa-118">name</span><span class="sxs-lookup"><span data-stu-id="cedfa-118">name</span></span></td>
<td><span data-ttu-id="cedfa-119">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="cedfa-119">Public.</span></span> <span data-ttu-id="cedfa-120">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cedfa-120">Required.</span></span> <span data-ttu-id="cedfa-121">Nome visualizzato della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cedfa-121">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="cedfa-122">tipo</span><span class="sxs-lookup"><span data-stu-id="cedfa-122">type</span></span></td>
<td><span data-ttu-id="cedfa-123">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="cedfa-123">Public.</span></span> <span data-ttu-id="cedfa-124">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cedfa-124">Required.</span></span> <span data-ttu-id="cedfa-125">Tipo di proprietà.</span><span class="sxs-lookup"><span data-stu-id="cedfa-125">The type of property.</span></span></td>
<td><span data-ttu-id="cedfa-126">Any: valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="cedfa-126">Any: Default.</span></span> <span data-ttu-id="cedfa-127">Il valore non verrà forzato dal sottosistema di proprietà.</span><span class="sxs-lookup"><span data-stu-id="cedfa-127">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="cedfa-128">VT_NULL verrà restituito da GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="cedfa-128">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="cedfa-129">Null: non è presente alcun valore per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cedfa-129">Null: There is no value for this property.</span></span> <span data-ttu-id="cedfa-130">VT_NULL verrà restituito da GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="cedfa-130">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="cedfa-131">Stringa: il valore deve essere un VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="cedfa-131">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="cedfa-132">Booleano: il valore deve essere un VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="cedfa-132">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="cedfa-133">Byte: il valore deve essere un VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="cedfa-133">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="cedfa-134">Buffer: il valore deve essere un VT_UI1 | VT_VECTOR buffer di byte.</span><span class="sxs-lookup"><span data-stu-id="cedfa-134">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="cedfa-135">Int16: il valore deve essere un VT_I2.</span><span class="sxs-lookup"><span data-stu-id="cedfa-135">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="cedfa-136">UInt16: il valore deve essere un VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="cedfa-136">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="cedfa-137">Int32: il valore deve essere un VT_I4.</span><span class="sxs-lookup"><span data-stu-id="cedfa-137">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="cedfa-138">UInt32: il valore deve essere un VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="cedfa-138">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="cedfa-139">Int64: il valore deve essere un VT_I8.</span><span class="sxs-lookup"><span data-stu-id="cedfa-139">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="cedfa-140">UInt64: il valore deve essere un VT_UI8</span><span class="sxs-lookup"><span data-stu-id="cedfa-140">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="cedfa-141">Double: il valore deve essere un VT_R8.</span><span class="sxs-lookup"><span data-stu-id="cedfa-141">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="cedfa-142">DateTime: il valore deve essere un VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="cedfa-142">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="cedfa-143">GUID: il valore deve essere un VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="cedfa-143">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="cedfa-144">BLOB: il valore deve essere un VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="cedfa-144">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="cedfa-145">Oggetto: il valore deve essere un VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="cedfa-145">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="cedfa-146">Stream: il valore deve essere un VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="cedfa-146">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="cedfa-147">Appunti: il valore deve essere un VT_CF.</span><span class="sxs-lookup"><span data-stu-id="cedfa-147">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cedfa-148">schema</span><span class="sxs-lookup"><span data-stu-id="cedfa-148">schema</span></span></td>
<td><span data-ttu-id="cedfa-149">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="cedfa-149">Public.</span></span> <span data-ttu-id="cedfa-150">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="cedfa-150">Optional.</span></span> <span data-ttu-id="cedfa-151">Schema in cui è definita la proprietà.</span><span class="sxs-lookup"><span data-stu-id="cedfa-151">The schema where the property is defined.</span></span></td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="cedfa-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="cedfa-152">Remarks</span></span>

<span data-ttu-id="cedfa-153">I connettori di ricerca OpenSearch possono usare la proprietà OpenSearchHTMLRolloverTemplate.</span><span class="sxs-lookup"><span data-stu-id="cedfa-153">OpenSearch search connectors can use the OpenSearchHTMLRolloverTemplate property.</span></span> <span data-ttu-id="cedfa-154">Questa proprietà identifica un modello formattato dopo la convenzione del modello OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="cedfa-154">This property identifies a template that is formatted following the OpenSearch template convention.</span></span> <span data-ttu-id="cedfa-155">Il modello OpenSearchHTMLRolloverTemplate viene usato quando l'utente fa clic sul pulsante "Cerca nel sito Web" sulla barra dei comandi.</span><span class="sxs-lookup"><span data-stu-id="cedfa-155">The OpenSearchHTMLRolloverTemplate template is used when the user clicks on the "Search on website" button in the command bar.</span></span>

## <a name="example"></a><span data-ttu-id="cedfa-156">Esempio</span><span class="sxs-lookup"><span data-stu-id="cedfa-156">Example</span></span>

<span data-ttu-id="cedfa-157">Nell'esempio seguente viene illustrato un <propertyStore> elemento con due <property> elementi.</span><span class="sxs-lookup"><span data-stu-id="cedfa-157">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



