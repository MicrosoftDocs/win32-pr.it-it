---
description: <locationProvider>L'elemento facoltativo specifica il provider di ricerca che deve essere usato dal connettore di ricerca del provider di servizi Web. Questo elemento contiene un attributo obbligatorio e un elemento figlio facoltativo.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Elemento locationProvider (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21101fd0e7c57b73af7bc9de525baaca9583d11e425b168d806f750063ac7203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711041"
---
# <a name="locationprovider-element-search-connector-schema"></a>Elemento locationProvider (schema del connettore di ricerca)

<locationProvider>L'elemento facoltativo specifica il provider di ricerca che deve essere usato dal connettore di ricerca del provider di servizi Web. Questo elemento contiene un attributo obbligatorio e un elemento figlio facoltativo.

## <a name="syntax"></a>Sintassi


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                                                   | Elementi figlio                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) | [Elemento propertyBag (schema del connettore di ricerca)](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | Obbligatorio. Identificatore di classe (CLSID) del provider di ricerca. |
| codebase  | facoltativo.                                                      |



 

## <a name="remarks"></a>Commenti

Il valore dell'attributo per il @clsid provider OpenSearch è {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.

I connettori di ricerca basati sul gestore di file system e di protocollo possono invece usare [<simpleLocation>](search-schema-sconn-simplelocation.md) l'elemento . Se <locationProvider> è presente, NON DEVE essere presente un <simpleLocation> elemento nella descrizione del connettore di ricerca.

## <a name="example-of-a-locationprovider-element"></a>Esempio di elemento locationProvider


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



