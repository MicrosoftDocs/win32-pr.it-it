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
# <a name="property-element-of-locationprovider-search-connector-schema"></a>Elemento Property di locationProvider (schema del connettore di ricerca)

L' <property> elemento facoltativo specifica le proprietà utilizzate dal provider di posizione. Queste proprietà sono specifiche di questo provider di località, quindi non esiste alcun set predefinito di nomi da usare. L' <property> elemento dispone di due attributi, come descritto in questo argomento.

## <a name="syntax"></a>Sintassi


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



## <a name="property-element-information"></a><property> Informazioni sugli elementi



| Elemento padre                                                                                 | Elementi figlio                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [Elemento locationProvider (schema del connettore di ricerca)](search-schema-sconn-locationprovider.md) | , descritta in questo argomento. |



 


## <a name="property-attributes"></a><property> Attributi



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
<td>Obbligatorio. Nome visualizzato della proprietà.</td>
<td> </td>
</tr>
<tr class="even">
<td>tipo</td>
<td>Obbligatorio. Tipo di proprietà.</td>
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
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Per il provider OpenSearch vengono usate le proprietà seguenti:

-   OpenSearchShortName: nome breve del servizio di ricerca
-   OpenSearchQueryTemplate: modello, formattato dopo la convenzione di modello OpenSearch, per il servizio query
-   MaximumResultCount: (numero) numero massimo di risultati restituiti dal servizio di ricerca
-   LinkIsFilePath: (booleano) se è true, il provider tenta di interpretare gli elementi restituiti come file, usando le estensioni per creare il ShellItem appropriato nella visualizzazione. Se false, gli elementi vengono considerati come collegamenti URL.

 

 



