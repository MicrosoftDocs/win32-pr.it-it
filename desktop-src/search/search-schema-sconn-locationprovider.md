---
description: L' <locationProvider> elemento facoltativo specifica il provider di ricerca che deve essere utilizzato dal connettore di ricerca del provider di servizi Web. Questo elemento contiene un attributo obbligatorio e un elemento figlio facoltativo.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Elemento locationProvider (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306082"
---
# <a name="locationprovider-element-search-connector-schema"></a>Elemento locationProvider (schema del connettore di ricerca)

L' <locationProvider> elemento facoltativo specifica il provider di ricerca che deve essere utilizzato dal connettore di ricerca del provider di servizi Web. Questo elemento contiene un attributo obbligatorio e un elemento figlio facoltativo.

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

Il @clsid valore dell'attributo per il provider OpenSearch è {48E277F6-4e74-4cd6-BA6F-FA4F42898223}.

I connettori di ricerca basati sul file System e sul gestore di protocollo possono usare [<simpleLocation>](search-schema-sconn-simplelocation.md) invece l'elemento. Se <locationProvider> è presente, non deve essere presente alcun <simpleLocation> elemento nella descrizione del connettore di ricerca.

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



 

 



