---
description: L' <propertyStore> elemento specifica un set di una o più proprietà utilizzate da questa libreria. Questo elemento è facoltativo e non ha attributi.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Elemento propertyStore (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980319"
---
# <a name="propertystore-element-library-schema"></a>Elemento propertyStore (schema della libreria)

L' <propertyStore> elemento specifica un set di una o più proprietà utilizzate da questa libreria. Questo elemento è facoltativo e non ha attributi.

## <a name="syntax"></a>Sintassi

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                               | Elementi figlio                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Elemento libraryDescription (schema della libreria)](schema-librarydescription.md) | [Elemento Property (schema della libreria)](schema-library-property.md) |



 

## <a name="remarks"></a>Commenti

L' <propertyStore> elemento può contenere uno o più <property> elementi figlio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Schema Descrizione libreria](library-schema-entry.md)
</dt> <dt>

[Cerca nello schema di descrizione del connettore](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
