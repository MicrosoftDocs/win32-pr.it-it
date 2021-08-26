---
description: <property>L'elemento specifica una proprietà utilizzata dalla libreria. Queste proprietà sono specifiche della libreria, quindi non esiste alcun set predefinito di nomi di proprietà da usare. Questo elemento è facoltativo e non ha elementi figlio.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Elemento property (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481122db633750b042172561eedace81fe1d752e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468638"
---
# <a name="property-element-library-schema"></a>Elemento property (schema della libreria)

<property>L'elemento specifica una proprietà utilizzata dalla libreria. Queste proprietà sono specifiche della libreria, quindi non esiste alcun set predefinito di nomi di proprietà da usare. Questo elemento è facoltativo e non ha elementi figlio.

## <a name="syntax"></a>Sintassi

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

## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                             | Elementi figlio |
|----------------------------------------------------------------------------|----------------|
| [Elemento propertyStore (schema della libreria)](schema-library-propertystore.md) | Nessuno           |



 

## <a name="attributes"></a>Attributi




| Attributo | Descrizione | Valori | 
|-----------|-------------|--------|
| name | Pubblica. Obbligatorio. Nome visualizzato della proprietà. | 
| tipo | Pubblica. Obbligatorio. Tipo di proprietà. | <ul><li>Qualsiasi: valore predefinito. Il valore non verrà forzato dal sottosistema di proprietà. VT_NULL verrà restituito da GetPropertyType.</li><li>Null: non è presente alcun valore per questa proprietà. VT_NULL verrà restituito da GetPropertyType.</li><li>Stringa: il valore deve essere un VT_LPWSTR.</li><li>Booleano: il valore deve essere un VT_BOOL.</li><li>Byte: il valore deve essere un VT_UI1.</li><li>Buffer: il valore deve essere un VT_UI1 | VT_VECTOR buffer di byte.</li><li>Int16: il valore deve essere un VT_I2.</li><li>UInt16: il valore deve essere un VT_UI2.</li><li>Int32: il valore deve essere un VT_I4.</li><li>UInt32: il valore deve essere un VT_UI4.</li><li>Int64: il valore deve essere un VT_I8.</li><li>UInt64: il valore deve essere un VT_UI8.</li><li>Double: il valore deve essere un VT_R8.</li><li>DateTime: il valore deve essere un VT_FILETIME.</li><li>GUID: il valore deve essere un VT_CLSID.</li><li>BLOB: il valore deve essere un VT_BLOB.</li><li>Oggetto: il valore deve essere un VT_UNKNOWN.</li><li>Stream: il valore deve essere un VT_STREAM.</li><li>Appunti: il valore deve essere un VT_CF.</li></ul> | 




 

## <a name="remarks"></a>Commenti

I requisiti per l'elemento <nome canonico> corrispondono ai requisiti per la ricerca Windows e il Windows delle proprietà. La stringa deve essere di tipo canonical-type.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Schema di descrizione della libreria](library-schema-entry.md)
</dt> <dt>

[Schemi proprietà](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[Schema di descrizione del connettore di ricerca](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
