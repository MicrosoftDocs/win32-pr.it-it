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
# <a name="property-element-of-propertystore-search-connector-schema"></a>Elemento Property di propertyStore (schema del connettore di ricerca)

L' <property> elemento facoltativo specifica una proprietà usata dal connettore di ricerca. Queste proprietà sono specifiche di questo connettore di ricerca, pertanto non esiste alcun set predefinito di nomi da usare. Questo elemento non ha elementi figlio.

## <a name="syntax"></a>Sintassi


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



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                           | Elementi figlio |
|------------------------------------------------------------------------------------------|----------------|
| [Elemento propertyStore (schema del connettore di ricerca)](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
<th>Valori</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name</td>
<td>Pubblica. Obbligatorio. Nome visualizzato della proprietà.</td>
<td> </td>
</tr>
<tr class="even">
<td>tipo</td>
<td>Pubblica. Obbligatorio. Tipo di proprietà.</td>
<td>Any: valore predefinito. Il valore non verrà forzato dal sottosistema di proprietà. VT_NULL verrà restituito da GetPropertyType.
<ul>
<li>Null: non è presente alcun valore per questa proprietà. VT_NULL verrà restituito da GetPropertyType.</li>
<li>Stringa: il valore deve essere un VT_LPWSTR.</li>
<li>Booleano: il valore deve essere un VT_BOOL.</li>
<li>Byte: il valore deve essere un VT_UI1.</li>
<li>Buffer: il valore deve essere un VT_UI1 | VT_VECTOR buffer di byte.</li>
<li>Int16: il valore deve essere un VT_I2.</li>
<li>UInt16: il valore deve essere un VT_UI2.</li>
<li>Int32: il valore deve essere un VT_I4.</li>
<li>UInt32: il valore deve essere un VT_UI4.</li>
<li>Int64: il valore deve essere un VT_I8.</li>
<li>UInt64: il valore deve essere un VT_UI8</li>
<li>Double: il valore deve essere un VT_R8.</li>
<li>DateTime: il valore deve essere un VT_FILETIME.</li>
<li>GUID: il valore deve essere un VT_CLSID.</li>
<li>BLOB: il valore deve essere un VT_BLOB.</li>
<li>Oggetto: il valore deve essere un VT_UNKNOWN.</li>
<li>Stream: il valore deve essere un VT_STREAM.</li>
<li>Appunti: il valore deve essere un VT_CF.</li>
</ul></td>
</tr>
<tr class="odd">
<td>schema</td>
<td>Pubblica. facoltativo. Schema in cui è definita la proprietà.</td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

I connettori di ricerca OpenSearch possono usare la proprietà OpenSearchHTMLRolloverTemplate. Questa proprietà identifica un modello formattato dopo la convenzione del modello OpenSearch. Il modello OpenSearchHTMLRolloverTemplate viene usato quando l'utente fa clic sul pulsante "Cerca nel sito Web" sulla barra dei comandi.

## <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato un <propertyStore> elemento con due <property> elementi.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



