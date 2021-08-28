---
description: Questo &lt; elemento searchConnectorDescriptionList contiene un elenco di connettori di ricerca mappati alle &gt; posizioni incluse in questa libreria. Ogni connettore di ricerca è definito da un &lt; elemento searchConnectorDescription. &gt; Questo elemento è facoltativo e non ha attributi.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Elemento searchConnectorDescriptionList (schema di libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc3a3cb7353529dccca66ffa15e1604bdd1c0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885607"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>Elemento searchConnectorDescriptionList (schema di libreria)

Questo &lt; elemento searchConnectorDescriptionList contiene un elenco di connettori di ricerca mappati alle &gt; posizioni incluse in questa libreria. Ogni connettore di ricerca è definito da un &lt; elemento searchConnectorDescription. &gt; Questo elemento è facoltativo e non ha attributi.

## <a name="syntax"></a>Sintassi

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                               | Elementi figlio                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Elemento libraryDescription (schema della libreria)](schema-librarydescription.md) | [Elemento searchConnectorDescription (schema della libreria)](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a>Commenti

I connettori di ricerca per Windows di ricerca federata e gli ambiti del gestore di protocollo non possono essere inclusi in una libreria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Schema di descrizione della libreria](library-schema-entry.md)
</dt> <dt>

[Schema di descrizione del connettore di ricerca](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
