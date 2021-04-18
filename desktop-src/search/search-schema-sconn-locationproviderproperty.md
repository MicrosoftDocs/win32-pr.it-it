---
description: L' <property> elemento facoltativo specifica le proprietà utilizzate dal provider di posizione.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Elemento Property di locationProvider (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322031"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a><span data-ttu-id="26caa-103">Elemento Property di locationProvider (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="26caa-103">property Element of locationProvider (Search Connector Schema)</span></span>

<span data-ttu-id="26caa-104">L' <property> elemento facoltativo specifica le proprietà utilizzate dal provider di posizione.</span><span class="sxs-lookup"><span data-stu-id="26caa-104">The optional <property> element specifies the properties used by the location provider.</span></span> <span data-ttu-id="26caa-105">Queste proprietà sono specifiche di questo provider di località, quindi non esiste alcun set predefinito di nomi da usare.</span><span class="sxs-lookup"><span data-stu-id="26caa-105">These properties are specific to this location provider, so there is no predefined set of names to use.</span></span> <span data-ttu-id="26caa-106">L' <property> elemento dispone di due attributi, come descritto in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="26caa-106">The <property> element has two attributes, as described in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="26caa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26caa-107">Syntax</span></span>


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
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



## <a name="property-element-information"></a><span data-ttu-id="26caa-108"><property> Informazioni sugli elementi</span><span class="sxs-lookup"><span data-stu-id="26caa-108"><property> Element Information</span></span>



| <span data-ttu-id="26caa-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="26caa-109">Parent Element</span></span>                                                                                 | <span data-ttu-id="26caa-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="26caa-110">Child Elements</span></span>                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="26caa-111">Elemento locationProvider (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="26caa-111">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md) | <span data-ttu-id="26caa-112">, descritta in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="26caa-112">property, described in this topic.</span></span> |



 


## <a name="property-attributes"></a><span data-ttu-id="26caa-113"><property> Attributi</span><span class="sxs-lookup"><span data-stu-id="26caa-113"><property> Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26caa-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="26caa-114">Attribute</span></span></th>
<th><span data-ttu-id="26caa-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26caa-115">Description</span></span></th>
<th><span data-ttu-id="26caa-116">Valori</span><span class="sxs-lookup"><span data-stu-id="26caa-116">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26caa-117">name</span><span class="sxs-lookup"><span data-stu-id="26caa-117">name</span></span></td>
<td><span data-ttu-id="26caa-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="26caa-118">Required.</span></span> <span data-ttu-id="26caa-119">Nome visualizzato della proprietà.</span><span class="sxs-lookup"><span data-stu-id="26caa-119">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="26caa-120">tipo</span><span class="sxs-lookup"><span data-stu-id="26caa-120">type</span></span></td>
<td><span data-ttu-id="26caa-121">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="26caa-121">Required.</span></span> <span data-ttu-id="26caa-122">Tipo di proprietà.</span><span class="sxs-lookup"><span data-stu-id="26caa-122">The type of property.</span></span></td>
<td><span data-ttu-id="26caa-123">Any: valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="26caa-123">Any: Default.</span></span> <span data-ttu-id="26caa-124">Il valore non verrà forzato dal sottosistema di proprietà.</span><span class="sxs-lookup"><span data-stu-id="26caa-124">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="26caa-125">VT_NULL verrà restituito da GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="26caa-125">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="26caa-126">Null: non è presente alcun valore per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="26caa-126">Null: There is no value for this property.</span></span> <span data-ttu-id="26caa-127">VT_NULL verrà restituito da GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="26caa-127">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="26caa-128">Stringa: il valore deve essere un VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="26caa-128">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="26caa-129">Booleano: il valore deve essere un VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="26caa-129">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="26caa-130">Byte: il valore deve essere un VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="26caa-130">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="26caa-131">Buffer: il valore deve essere un VT_UI1 | VT_VECTOR buffer di byte.</span><span class="sxs-lookup"><span data-stu-id="26caa-131">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="26caa-132">Int16: il valore deve essere un VT_I2.</span><span class="sxs-lookup"><span data-stu-id="26caa-132">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="26caa-133">UInt16: il valore deve essere un VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="26caa-133">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="26caa-134">Int32: il valore deve essere un VT_I4.</span><span class="sxs-lookup"><span data-stu-id="26caa-134">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="26caa-135">UInt32: il valore deve essere un VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="26caa-135">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="26caa-136">Int64: il valore deve essere un VT_I8.</span><span class="sxs-lookup"><span data-stu-id="26caa-136">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="26caa-137">UInt64: il valore deve essere un VT_UI8</span><span class="sxs-lookup"><span data-stu-id="26caa-137">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="26caa-138">Double: il valore deve essere un VT_R8.</span><span class="sxs-lookup"><span data-stu-id="26caa-138">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="26caa-139">DateTime: il valore deve essere un VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="26caa-139">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="26caa-140">GUID: il valore deve essere un VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="26caa-140">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="26caa-141">BLOB: il valore deve essere un VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="26caa-141">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="26caa-142">Oggetto: il valore deve essere un VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="26caa-142">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="26caa-143">Stream: il valore deve essere un VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="26caa-143">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="26caa-144">Appunti: il valore deve essere un VT_CF.</span><span class="sxs-lookup"><span data-stu-id="26caa-144">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="26caa-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="26caa-145">Remarks</span></span>

<span data-ttu-id="26caa-146">Per il provider OpenSearch vengono usate le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="26caa-146">For the OpenSearch provider, the following properties are used:</span></span>

-   <span data-ttu-id="26caa-147">OpenSearchShortName: nome breve del servizio di ricerca</span><span class="sxs-lookup"><span data-stu-id="26caa-147">OpenSearchShortName: Short name of the search service</span></span>
-   <span data-ttu-id="26caa-148">OpenSearchQueryTemplate: modello, formattato dopo la convenzione di modello OpenSearch, per il servizio query</span><span class="sxs-lookup"><span data-stu-id="26caa-148">OpenSearchQueryTemplate: Template, formatted following the OpenSearch template convention, for the query service</span></span>
-   <span data-ttu-id="26caa-149">MaximumResultCount: (numero) numero massimo di risultati restituiti dal servizio di ricerca</span><span class="sxs-lookup"><span data-stu-id="26caa-149">MaximumResultCount: (number) Maximum number of results returned by the search service</span></span>
-   <span data-ttu-id="26caa-150">LinkIsFilePath: (booleano) se è true, il provider tenta di interpretare gli elementi restituiti come file, usando le estensioni per creare il ShellItem appropriato nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="26caa-150">LinkIsFilePath: (Boolean) If true, the provider tries to interpret returned items as files, using their extensions to create the proper ShellItem in the view.</span></span> <span data-ttu-id="26caa-151">Se false, gli elementi vengono considerati come collegamenti URL.</span><span class="sxs-lookup"><span data-stu-id="26caa-151">If false, items are treated as URL shortcuts.</span></span>

 

 



