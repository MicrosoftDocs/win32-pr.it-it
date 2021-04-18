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
# <a name="datadefinitiontype-complex-type"></a>Tipo complesso DataDefinitionType

Definisce un elemento di dati che si desidera includere nell'evento.

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

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>count</td>
<td><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></td>
<td>Il numero di elementi nella matrice se l'elemento dati è una matrice. È possibile specificare il conteggio effettivo o il nome di un altro elemento di dati che contiene il conteggio. <br/></td>
</tr>
<tr class="even">
<td>inType</td>
<td><strong>QName</strong></td>
<td>Tipo di dati per questo elemento di dati. Per un elenco di tipi di dati di input predefiniti, vedere il tipo complesso <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td>length</td>
<td><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></td>
<td>Lunghezza di un elemento di dati a lunghezza variabile, ad esempio un BLOB binario. Per i dati binari, specificare la lunghezza in byte e per i dati di tipo stringa, specificare la lunghezza in caratteri. È possibile specificare la lunghezza effettiva o il nome di un altro elemento di dati che contiene la lunghezza.<br/> Se si usa l'attributo length per specificare una stringa a lunghezza fissa, è necessario aggiungere la stringa alla lunghezza fissa consentendo il carattere di terminazione null alla fine. ad esempio, se la lunghezza è 5, la stringa &quot; ABC &quot; deve essere riempita come &quot; ABC &quot; . La lunghezza della stringa deve includere il carattere di terminazione null.<br/></td>
</tr>
<tr class="even">
<td>map</td>
<td>string</td>
<td>Nome del mapping nome/valore da utilizzare per eseguire il mapping dei valori interi alle stringhe. Il tipo di dati dell'elemento dati deve essere uno dei tipi seguenti:<br/>
<ul>
<li>win:UInt8</li>
<li>win:UInt16</li>
<li>win:UInt32</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>
<td>string</td>
<td>Nome dell'elemento dati. È possibile usare il nome per fare riferimento a questo elemento di dati nel frammento XML se si specifica una sezione <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> nel modello. È anche possibile fare riferimento a questo nome in un attributo length o count di un altro elemento di dati se questo elemento dati contiene la lunghezza o il valore Count.<br/> <strong>Windows Vista:</strong> Questo attributo è facoltativo.<br/></td>
</tr>
<tr class="even">
<td>outtype</td>
<td><strong>QName</strong></td>
<td>Tipo di dati da utilizzare per il rendering dell'elemento di dati. Per un elenco di tipi di dati di output predefiniti, vedere il tipo complesso <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> .<br/> <strong>Windows Vista:</strong> Il tipo di output viene ignorato e il servizio determina il tipo in base al tipo di input.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Per i tipi di input a lunghezza variabile, ad esempio i BLOB binari, è necessario usare l'attributo length per specificare in modo esplicito le dimensioni dei dati. Per le stringhe, specificare l'attributo length solo se le stringhe hanno una lunghezza fissa.

## <a name="examples"></a>Esempio

Di seguito sono riportati alcuni esempi delle definizioni degli elementi di dati.


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





