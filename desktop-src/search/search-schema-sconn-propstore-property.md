---
description: "&lt;L'elemento &gt; proprietà facoltativo specifica una proprietà usata dal connettore di ricerca. Queste proprietà sono specifiche di questo connettore di ricerca, quindi non esiste alcun set predefinito di nomi da usare. Questo elemento non ha elementi figlio."
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Elemento property di propertyStore (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ad97c22ac87d67fdec0d007d4333bffe16aad1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886781"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>Elemento property di propertyStore (schema del connettore di ricerca)

&lt;L'elemento &gt; proprietà facoltativo specifica una proprietà usata dal connettore di ricerca. Queste proprietà sono specifiche di questo connettore di ricerca, quindi non esiste alcun set predefinito di nomi da usare. Questo elemento non ha elementi figlio.

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




| Attributo | Descrizione | Valori | 
|-----------|-------------|--------|
| name | Pubblica. Obbligatorio. Nome visualizzato della proprietà. |   | 
| tipo | Pubblica. Obbligatorio. Tipo di proprietà. | Qualsiasi: valore predefinito. Il valore non verrà forzato dal sottosistema di proprietà. VT_NULL verrà restituito da GetPropertyType.<ul><li>Null: non è presente alcun valore per questa proprietà. VT_NULL verrà restituito da GetPropertyType.</li><li>Stringa: il valore deve essere un VT_LPWSTR.</li><li>Boolean: il valore deve essere un VT_BOOL.</li><li>Byte: il valore deve essere un VT_UI1.</li><li>Buffer: il valore deve essere un VT_UI1 | VT_VECTOR buffer di byte.</li><li>Int16: il valore deve essere un VT_I2.</li><li>UInt16: il valore deve essere un VT_UI2.</li><li>Int32: il valore deve essere un VT_I4.</li><li>UInt32: il valore deve essere un VT_UI4.</li><li>Int64: il valore deve essere un VT_I8.</li><li>UInt64: il valore deve essere un VT_UI8</li><li>Double: il valore deve essere un VT_R8.</li><li>DateTime: il valore deve essere un VT_FILETIME.</li><li>GUID: il valore deve essere un VT_CLSID.</li><li>BLOB: il valore deve essere un VT_BLOB.</li><li>Oggetto: il valore deve essere un VT_UNKNOWN.</li><li>Stream: il valore deve essere un VT_STREAM.</li><li>Appunti: il valore deve essere un VT_CF.</li></ul> | 
| schema | Pubblica. facoltativo. Schema in cui è definita la proprietà. |   | 




 

## <a name="remarks"></a>Commenti

OpenSearch connettori di ricerca possono usare la proprietà OpenSearchHTMLRolloverTemplate. Questa proprietà identifica un modello formattato in base alla convenzione OpenSearch modello. Il modello OpenSearchHTMLRolloverTemplate viene usato quando l'utente fa clic sul pulsante "Cerca nel sito Web" nella barra dei comandi.

## <a name="example"></a>Esempio

L'esempio seguente mostra un &lt; elemento propertyStore &gt; con due &lt; elementi &gt; property.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



