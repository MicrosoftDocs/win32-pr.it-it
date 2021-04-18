---
description: Specifica come configurare il motore di ricerca di Windows rispetto a una definizione di proprietà specificata.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310111"
---
# <a name="searchinfo"></a><span data-ttu-id="e16d6-103">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e16d6-103">searchInfo</span></span>

<span data-ttu-id="e16d6-104">Specifica come configurare il motore di ricerca di Windows rispetto a una definizione di proprietà specificata.</span><span class="sxs-lookup"><span data-stu-id="e16d6-104">Specifies how to configure the Windows search engine with respect to a given property definition.</span></span> <span data-ttu-id="e16d6-105">Se non viene specificato alcun elemento [searchInfo]() , la proprietà non viene inclusa nel motore di ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="e16d6-105">If no [searchInfo]() element is provided, then the property is not included in the Windows search engine.</span></span> <span data-ttu-id="e16d6-106">Questo elemento è stato modificato per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e16d6-106">This element has changed for Windows 7.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="e16d6-107">Sintassi per Windows 7</span><span class="sxs-lookup"><span data-stu-id="e16d6-107">Syntax for Windows 7</span></span>


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a><span data-ttu-id="e16d6-108">Sintassi per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e16d6-108">Syntax for Windows Vista</span></span>


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="e16d6-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e16d6-109">Element Information</span></span>



| <span data-ttu-id="e16d6-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e16d6-110">Parent Element</span></span>                                                   | <span data-ttu-id="e16d6-111">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e16d6-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="e16d6-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e16d6-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="e16d6-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="e16d6-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="e16d6-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="e16d6-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e16d6-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="e16d6-115">Attribute</span></span></th>
<th><span data-ttu-id="e16d6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e16d6-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e16d6-117">inInvertedIndex</span><span class="sxs-lookup"><span data-stu-id="e16d6-117">inInvertedIndex</span></span></td>
<td><span data-ttu-id="e16d6-118">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="e16d6-118">Public.</span></span> <span data-ttu-id="e16d6-119">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e16d6-119">Optional.</span></span> <span data-ttu-id="e16d6-120">Indica se il valore della proprietà deve essere archiviato nell'indice invertito.</span><span class="sxs-lookup"><span data-stu-id="e16d6-120">Indicates whether the property value should be stored in the inverted index.</span></span> <span data-ttu-id="e16d6-121">Ciò consente agli utenti finali di eseguire query full-text sui valori di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="e16d6-121">This lets end users perform full-text queries over the values of this property.</span></span> <span data-ttu-id="e16d6-122">Il valore predefinito è &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="e16d6-122">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e16d6-123">isColumn</span><span class="sxs-lookup"><span data-stu-id="e16d6-123">isColumn</span></span></td>
<td><span data-ttu-id="e16d6-124">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="e16d6-124">Public.</span></span> <span data-ttu-id="e16d6-125">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e16d6-125">Optional.</span></span> <span data-ttu-id="e16d6-126">Indica se la proprietà deve essere archiviata anche nel database di ricerca di Windows come colonna, in modo che i fornitori di software indipendenti (ISV) possano creare query basate su predicato (ad esempio, &quot; Select \* where &quot; System. title &quot; =' qqq ' &quot; ).</span><span class="sxs-lookup"><span data-stu-id="e16d6-126">Indicates whether the property should also be stored in the Windows search database as a column, so that independent software vendors (ISVs) can create predicate-based queries (for example, &quot;Select \* Where &quot;System.Title&quot;='qqq'&quot;).</span></span> <span data-ttu-id="e16d6-127">Se l'autore dello schema desidera consentire agli utenti finali o agli sviluppatori di creare query basate su predicati sulle proprietà, è necessario impostare questa proprietà su &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="e16d6-127">If the schema creator wants to enable end users (or developers) to create predicate based queries on the properties, then this needs to be set to &quot;true&quot;.</span></span> <span data-ttu-id="e16d6-128">Il valore predefinito è &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="e16d6-128">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e16d6-129">isColumnSparse</span><span class="sxs-lookup"><span data-stu-id="e16d6-129">isColumnSparse</span></span></td>
<td><span data-ttu-id="e16d6-130">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="e16d6-130">Public.</span></span> <span data-ttu-id="e16d6-131">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e16d6-131">Optional.</span></span> <span data-ttu-id="e16d6-132">Il valore predefinito è &quot;True&quot;.</span><span class="sxs-lookup"><span data-stu-id="e16d6-132">The default is &quot;true&quot;.</span></span> <span data-ttu-id="e16d6-133">Se la proprietà è multivalore, questo attributo è sempre &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="e16d6-133">If the property is multi-valued, this attribute is always &quot;true&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e16d6-134">columnIndexType</span><span class="sxs-lookup"><span data-stu-id="e16d6-134">columnIndexType</span></span></td>
<td><span data-ttu-id="e16d6-135">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="e16d6-135">Public.</span></span> <span data-ttu-id="e16d6-136">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e16d6-136">Optional.</span></span> <span data-ttu-id="e16d6-137">Per ottimizzare l'ordinamento e il raggruppamento, il motore di ricerca di Windows può creare indici secondari per le proprietà con la colonna = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="e16d6-137">To optimize sorting and grouping, the Windows search engine can create secondary indexes for properties that have isColumn=&quot;true&quot;.</span></span> <span data-ttu-id="e16d6-138">Questo attributo è utile solo quando inInvertedIndex è &quot; true &quot; in Windows Vista o quando la colonna è &quot; true &quot; in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e16d6-138">This attribute is only useful when inInvertedIndex is &quot;true&quot; in Windows Vista or when isColumn is &quot;true&quot; in Windows 7.</span></span> <span data-ttu-id="e16d6-139">Se la proprietà tende a essere ordinata spesso dagli utenti, è necessario specificare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="e16d6-139">If the property tends to be sorted frequently by users, this attribute should be specified.</span></span> <span data-ttu-id="e16d6-140">Il valore predefinito in Windows Vista è &quot; NotIndexed &quot; .</span><span class="sxs-lookup"><span data-stu-id="e16d6-140">The default value in Windows Vista is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="e16d6-141">Il valore predefinito in Windows 7 è &quot; OnDemand &quot; .</span><span class="sxs-lookup"><span data-stu-id="e16d6-141">The default value in Windows 7 is &quot;OnDemand&quot;.</span></span> <span data-ttu-id="e16d6-142">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="e16d6-142">The following values are valid.</span></span>
<ul>
<li><span data-ttu-id="e16d6-143"><strong>NotIndexed</strong>: mai compilare un indice di valore.</span><span class="sxs-lookup"><span data-stu-id="e16d6-143"><strong>NotIndexed</strong>: Never build a value index.</span></span></li>
<li><span data-ttu-id="e16d6-144"><strong>Ondisk</strong>: compilare un indice valore per impostazione predefinita per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="e16d6-144"><strong>OnDisk</strong>: Build a value index by default for this property.</span></span></li>
<li><span data-ttu-id="e16d6-145"><strong>OnDiskAll</strong> (solo Windows 7 e versioni successive): compilare un indice valore per impostazione predefinita per questa proprietà e, se si tratta di una proprietà Vector, anche un indice valore per tutti i valori vettoriali concatenati.</span><span class="sxs-lookup"><span data-stu-id="e16d6-145"><strong>OnDiskAll</strong> (Windows 7 and later only): Build a value index by default for this property, and if it is a vector property, also a value index for all concatenated vector values.</span></span></li>
<li><span data-ttu-id="e16d6-146"><strong>OnDiskVector</strong> (solo Windows 7 e versioni successive): compilare un indice valore per impostazione predefinita per i valori vettoriali concatenati.</span><span class="sxs-lookup"><span data-stu-id="e16d6-146"><strong>OnDiskVector</strong> (Windows 7 and later only): Build a value index by default for the concatenated vector values.</span></span></li>
<li><span data-ttu-id="e16d6-147"><strong>OnDemand</strong> (solo Windows 7 e versioni successive): solo gli indici del valore di compilazione per richiesta, ovvero solo la prima volta che vengono usati per una query.</span><span class="sxs-lookup"><span data-stu-id="e16d6-147"><strong>OnDemand</strong> (Windows 7 and later only): Only build value indices by demand, that is, only first time they are used for a query.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e16d6-148">maxSize</span><span class="sxs-lookup"><span data-stu-id="e16d6-148">maxSize</span></span></td>
<td><span data-ttu-id="e16d6-149">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="e16d6-149">Public.</span></span> <span data-ttu-id="e16d6-150">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e16d6-150">Optional.</span></span> <span data-ttu-id="e16d6-151">Dimensione massima, in byte, consentita per una determinata proprietà archiviata nel database di ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="e16d6-151">The maximum size, in bytes, allowed for a certain property that is stored in the Windows search database.</span></span> <span data-ttu-id="e16d6-152">Il valore predefinito è:</span><span class="sxs-lookup"><span data-stu-id="e16d6-152">The default is:</span></span>
<ul>
<li><span data-ttu-id="e16d6-153"><strong>Windows Vista</strong>: 128 byte</span><span class="sxs-lookup"><span data-stu-id="e16d6-153"><strong>Windows Vista</strong>: 128 bytes</span></span></li>
<li><span data-ttu-id="e16d6-154"><strong>Windows 7 e versioni successive</strong>: 512 byte</span><span class="sxs-lookup"><span data-stu-id="e16d6-154"><strong>Windows 7 and later</strong>: 512 bytes</span></span></li>
</ul>
<span data-ttu-id="e16d6-155">Si noti che questa dimensione massima viene misurata in byte, non in caratteri.</span><span class="sxs-lookup"><span data-stu-id="e16d6-155">Note that this maximum size is measured in bytes, not characters.</span></span> <span data-ttu-id="e16d6-156">Il numero massimo di caratteri dipende dalla codifica.</span><span class="sxs-lookup"><span data-stu-id="e16d6-156">The maximum number of characters depends on their encoding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e16d6-157">tasti di scelta</span><span class="sxs-lookup"><span data-stu-id="e16d6-157">mnemonics</span></span></td>
<td><span data-ttu-id="e16d6-158"><strong>Windows 7 e versioni successive.</strong></span><span class="sxs-lookup"><span data-stu-id="e16d6-158"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="e16d6-159">Pubblica.</span><span class="sxs-lookup"><span data-stu-id="e16d6-159">Public.</span></span> <span data-ttu-id="e16d6-160">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e16d6-160">Optional.</span></span> <span data-ttu-id="e16d6-161">Elenco di valori mnemonico che possono essere usati per fare riferimento alla proprietà nelle query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e16d6-161">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="e16d6-162">L'elenco è delimitato dal carattere "|".</span><span class="sxs-lookup"><span data-stu-id="e16d6-162">The list is delimited with the '|' character.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
