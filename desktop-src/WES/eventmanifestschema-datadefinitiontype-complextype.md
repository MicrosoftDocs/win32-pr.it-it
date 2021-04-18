---
title: Tipo complesso DataDefinitionType
description: Definisce un elemento di dati che si desidera includere nell'evento. | Tipo complesso DataDefinitionType
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- Log eventi di tipo complesso DataDefinitionType
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19584c28a7bdf7ae01b87d1f414b9464b7b4271d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321264"
---
# <a name="datadefinitiontype-complex-type"></a><span data-ttu-id="0e4f3-105">Tipo complesso DataDefinitionType</span><span class="sxs-lookup"><span data-stu-id="0e4f3-105">DataDefinitionType Complex Type</span></span>

<span data-ttu-id="0e4f3-106">Definisce un elemento di dati che si desidera includere nell'evento.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-106">Defines a data item that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="DataDefinitionType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="inType"
                type="QName"
                use="required"
             />
            <xs:attribute name="outType"
                type="QName"
                use="optional"
             />
            <xs:attribute name="map"
                type="string"
                use="optional"
             />
            <xs:attribute name="length"
                type="LengthType"
                use="optional"
             />
            <xs:attribute name="count"
                type="CountType"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="0e4f3-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="0e4f3-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0e4f3-108">Nome</span><span class="sxs-lookup"><span data-stu-id="0e4f3-108">Name</span></span></th>
<th><span data-ttu-id="0e4f3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e4f3-109">Type</span></span></th>
<th><span data-ttu-id="0e4f3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e4f3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e4f3-111">count</span><span class="sxs-lookup"><span data-stu-id="0e4f3-111">count</span></span></td>
<td><span data-ttu-id="0e4f3-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e4f3-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></span></span></td>
<td><span data-ttu-id="0e4f3-113">Il numero di elementi nella matrice se l'elemento dati è una matrice.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-113">The number of elements in the array if the data item is an array.</span></span> <span data-ttu-id="0e4f3-114">È possibile specificare il conteggio effettivo o il nome di un altro elemento di dati che contiene il conteggio.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-114">You can specify the actual count or the name of another data item that contains the count.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e4f3-115">inType</span><span class="sxs-lookup"><span data-stu-id="0e4f3-115">inType</span></span></td>
<td><span data-ttu-id="0e4f3-116"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="0e4f3-116"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="0e4f3-117">Tipo di dati per questo elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-117">The data type for this data item.</span></span> <span data-ttu-id="0e4f3-118">Per un elenco di tipi di dati di input predefiniti, vedere il tipo complesso <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0e4f3-118">For a list of predefined input data types, see the <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e4f3-119">length</span><span class="sxs-lookup"><span data-stu-id="0e4f3-119">length</span></span></td>
<td><span data-ttu-id="0e4f3-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></span><span class="sxs-lookup"><span data-stu-id="0e4f3-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></span></span></td>
<td><span data-ttu-id="0e4f3-121">Lunghezza di un elemento di dati a lunghezza variabile, ad esempio un BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-121">The length of a variable length data item, such as a binary blob.</span></span> <span data-ttu-id="0e4f3-122">Per i dati binari, specificare la lunghezza in byte e per i dati di tipo stringa, specificare la lunghezza in caratteri.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-122">For binary data, specify the length in bytes and for string data, specify the length in characters.</span></span> <span data-ttu-id="0e4f3-123">È possibile specificare la lunghezza effettiva o il nome di un altro elemento di dati che contiene la lunghezza.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-123">You can specify the actual length or the name of another data item that contains the length.</span></span><br/> <span data-ttu-id="0e4f3-124">Se si usa l'attributo length per specificare una stringa a lunghezza fissa, è necessario aggiungere la stringa alla lunghezza fissa consentendo il carattere di terminazione null alla fine. ad esempio, se la lunghezza è 5, la stringa &quot; ABC &quot; deve essere riempita come &quot; ABC &quot; .</span><span class="sxs-lookup"><span data-stu-id="0e4f3-124">If you use the length attribute to specify a fixed length string, you must pad the string to its fixed length allowing for the null-terminator character at the end (for example, if the length is 5, the string &quot;abc&quot; must be padded as &quot;abc &quot;.</span></span> <span data-ttu-id="0e4f3-125">La lunghezza della stringa deve includere il carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-125">The string length must include the null-terminator character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e4f3-126">map</span><span class="sxs-lookup"><span data-stu-id="0e4f3-126">map</span></span></td>
<td><span data-ttu-id="0e4f3-127">string</span><span class="sxs-lookup"><span data-stu-id="0e4f3-127">string</span></span></td>
<td><span data-ttu-id="0e4f3-128">Nome del mapping nome/valore da utilizzare per eseguire il mapping dei valori interi alle stringhe.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-128">The name of the name/value map to use to map integer values to strings.</span></span> <span data-ttu-id="0e4f3-129">Il tipo di dati dell'elemento dati deve essere uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0e4f3-129">The data type of the data item must be of one of the following types:</span></span><br/>
<ul>
<li><span data-ttu-id="0e4f3-130">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="0e4f3-130">win:UInt8</span></span></li>
<li><span data-ttu-id="0e4f3-131">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="0e4f3-131">win:UInt16</span></span></li>
<li><span data-ttu-id="0e4f3-132">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="0e4f3-132">win:UInt32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e4f3-133">name</span><span class="sxs-lookup"><span data-stu-id="0e4f3-133">name</span></span></td>
<td><span data-ttu-id="0e4f3-134">string</span><span class="sxs-lookup"><span data-stu-id="0e4f3-134">string</span></span></td>
<td><span data-ttu-id="0e4f3-135">Nome dell'elemento dati.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-135">The name of the data item.</span></span> <span data-ttu-id="0e4f3-136">È possibile usare il nome per fare riferimento a questo elemento di dati nel frammento XML se si specifica una sezione <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> nel modello.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-136">You can use the name to reference this data item in your XML fragment if you specify a <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> section in your template.</span></span> <span data-ttu-id="0e4f3-137">È anche possibile fare riferimento a questo nome in un attributo length o count di un altro elemento di dati se questo elemento dati contiene la lunghezza o il valore Count.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-137">You can also reference this name in a length or count attribute of another data item if this data item contains its length or count value.</span></span><br/> <span data-ttu-id="0e4f3-138"><strong>Windows Vista:</strong> Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-138"><strong>Windows Vista:</strong> This attribute is optional.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e4f3-139">outtype</span><span class="sxs-lookup"><span data-stu-id="0e4f3-139">outType</span></span></td>
<td><span data-ttu-id="0e4f3-140"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="0e4f3-140"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="0e4f3-141">Tipo di dati da utilizzare per il rendering dell'elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-141">The data type to use when rendering this data item.</span></span> <span data-ttu-id="0e4f3-142">Per un elenco di tipi di dati di output predefiniti, vedere il tipo complesso <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0e4f3-142">For a list of predefined output data types, see the <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> complex type.</span></span><br/> <span data-ttu-id="0e4f3-143"><strong>Windows Vista:</strong> Il tipo di output viene ignorato e il servizio determina il tipo in base al tipo di input.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-143"><strong>Windows Vista:</strong> The output type is ignored, and the service determines the type based on the input type.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="0e4f3-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e4f3-144">Remarks</span></span>

<span data-ttu-id="0e4f3-145">Per i tipi di input a lunghezza variabile, ad esempio i BLOB binari, è necessario usare l'attributo length per specificare in modo esplicito le dimensioni dei dati.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-145">For variable length input types, such as binary blobs, you must use the length attribute to explicitly specify the size of the data.</span></span> <span data-ttu-id="0e4f3-146">Per le stringhe, specificare l'attributo length solo se le stringhe hanno una lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-146">For strings, specify the length attribute only if the strings are of a fixed length.</span></span>

## <a name="examples"></a><span data-ttu-id="0e4f3-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="0e4f3-147">Examples</span></span>

<span data-ttu-id="0e4f3-148">Di seguito sono riportati alcuni esempi delle definizioni degli elementi di dati.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-148">The following are a few examples of the data item definitions.</span></span>


```XML
<!-- The data item is an 8-bit integer -->
<data name="binaryChar" inType="win:UInt8">
 
<!-- The data item is a single ANSI character -->
<data name="ansiChar" inType="win:UInt8" outtype="xs:string">
 
<!-- The data item is a single Unicode character -->
<data name="unicodeChar" inType="win:UInt16" outtype="xs:string">
 
<!-- The data item is an IP address that is rendered as a dot separated list of interger values -->
<data name="ipAddress" inType="win:UInt32" outtype="win:IPv4">
 
<!-- The data item is a Boolean value -->
<data name="success" inType="win:boolean">
 
<!-- The data item is a null-terminated ANSI string -->
<data name="string" inType="win:AnsiString"> 

<!-- The data item is a fixed length ANSI string -->
<data name="string" inType="win:AnsiString" length="42"> 
 
<!-- The data item is a fixed length array of null-terminated ANSI strings -->
<data name="strings" inType="win:AnsiString" count="20">
 
<!-- The data item is a fixed length array of fixed length ANSI strings -->
<data name="strings" inType="win:AnsiString" length="42" count="20">
 
<!-- The data item is a variable length array of same sized ANSI strings -->
<data name="stringLength" inType="win:UInt16">
<data name="arrayCount" inType="win:Uint16">
<data name="strings" inType="win:AnsiString" length="stringLength" count="arrayCount"> 
 
<!-- For binary data, you must specify the size.
<!-- The data item is a fixed length array of fixed length binary blobs -->
<data name="blobs" inType="win:Binary" length="42" count="20">

<!-- The data item is a fixed length binary blob -->
<data name="blob" inType="win:Binary" length="42">

<!-- The following are illegal binary data definitions -->
<!-- This definition is illegal because no length is specified -->
<data name="blob" inType="win:Binary"> 
 
<!-- This definition is illegal because you cannot determine the length of each binary blob -->
<data name="blob" inType="win:Binary" count="20"> 
 
<!-- The data item is a variable length array of structures. Each structure -->
<!-- contains an array of same sized ANSI strings --> 
<data name="arrayStructCount" inType="win:UInt16">
<struct name="countedStrings" count="arrayStructCount">
      <data name="stringLength" inType="win:UInt16">
      <data name="string" inType="win:AnsiString" length="stringLength">
</struct>
 
<!-- The data item is a time stamp that is rendered in 100ns units -->
<data name="timestamp" inType="win:UInt32" outType="win:ETWTIME">

<!-- The data item is a fixed length array of integers --> 
<data name="integers" inType="win:UInt32" count="20">

<!-- The data item is a variable length array of integers -->
<data name="arrayCount" inType="win:UInt16"> 
<data name="integers" inType="win:UInt32" count="arrayCount"> 

<!-- The following is illegal because you cannot assign a length value to a data type of a known size -->
<data name="integer" inType="win:UInt32" length="42">
```



## <a name="requirements"></a><span data-ttu-id="0e4f3-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e4f3-149">Requirements</span></span>



| <span data-ttu-id="0e4f3-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e4f3-150">Requirement</span></span> | <span data-ttu-id="0e4f3-151">Valore</span><span class="sxs-lookup"><span data-stu-id="0e4f3-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e4f3-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e4f3-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0e4f3-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e4f3-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e4f3-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e4f3-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0e4f3-155">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e4f3-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





