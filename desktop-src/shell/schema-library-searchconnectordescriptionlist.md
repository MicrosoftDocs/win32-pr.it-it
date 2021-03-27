---
description: Questo <searchConnectorDescriptionList> elemento contiene un elenco di connettori di ricerca che eseguono il mapping alle posizioni incluse nella libreria. Ogni connettore di ricerca viene definito da un <searchConnectorDescription> elemento. Questo elemento è facoltativo e non ha attributi.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Elemento searchConnectorDescriptionList (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980463"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>Elemento searchConnectorDescriptionList (schema della libreria)

Questo <searchConnectorDescriptionList> elemento contiene un elenco di connettori di ricerca che eseguono il mapping alle posizioni incluse nella libreria. Ogni connettore di ricerca viene definito da un <searchConnectorDescription> elemento. Questo elemento è facoltativo e non ha attributi.

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

Non è possibile includere in una libreria i connettori di ricerca per gli ambiti di ricerca federata e di gestori di protocollo di Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Schema Descrizione libreria](library-schema-entry.md)
</dt> <dt>

[Cerca nello schema di descrizione del connettore](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
