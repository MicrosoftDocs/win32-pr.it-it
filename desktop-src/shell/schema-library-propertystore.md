---
description: <propertyStore>L'elemento specifica un set di una o più proprietà usate da questa libreria. Questo elemento è facoltativo e non ha attributi.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Elemento propertyStore (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ff30972a358916e715ff1b374a555c6db24ee6d512d114bcf47f57ac8a1954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452976"
---
# <a name="propertystore-element-library-schema"></a>Elemento propertyStore (schema della libreria)

<propertyStore>L'elemento specifica un set di una o più proprietà usate da questa libreria. Questo elemento è facoltativo e non ha attributi.

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
| [Elemento libraryDescription (schema della libreria)](schema-librarydescription.md) | [Elemento property (schema della libreria)](schema-library-property.md) |



 

## <a name="remarks"></a>Commenti

<propertyStore>L'elemento può avere uno o più elementi <property> figlio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Schema di descrizione della libreria](library-schema-entry.md)
</dt> <dt>

[Schema di descrizione del connettore di ricerca](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
