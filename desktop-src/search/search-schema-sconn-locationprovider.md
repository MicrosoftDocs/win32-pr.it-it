---
description: "&lt;L'elemento locationProvider &gt; facoltativo specifica il provider di ricerca che deve essere usato dal connettore di ricerca del provider di servizi Web. Questo elemento contiene un attributo obbligatorio e un elemento figlio facoltativo."
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Elemento locationProvider (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f049a01cc0c51075c147918a2f43b740000f2e36
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883363"
---
# <a name="locationprovider-element-search-connector-schema"></a>Elemento locationProvider (schema del connettore di ricerca)

&lt;L'elemento locationProvider &gt; facoltativo specifica il provider di ricerca che deve essere usato dal connettore di ricerca del provider di servizi Web. Questo elemento contiene un attributo obbligatorio e un elemento figlio facoltativo.

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

I connettori di ricerca basati sul gestore del file system e del protocollo possono invece usare [ &lt; l'elemento simpleLocation. &gt; ](search-schema-sconn-simplelocation.md) Se &lt; locationProvider &gt; è presente, non deve essere presente un elemento &lt; simpleLocation nella &gt; descrizione del connettore di ricerca.

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



 

 



