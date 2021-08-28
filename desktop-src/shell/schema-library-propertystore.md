---
description: "&lt;L'elemento propertyStore &gt; specifica un set di una o più proprietà usate da questa libreria. Questo elemento è facoltativo e non ha attributi."
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Elemento propertyStore (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089e87e6e7bdfa568ffa2e8903f6347cb6dc7b3d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880427"
---
# <a name="propertystore-element-library-schema"></a>Elemento propertyStore (schema della libreria)

&lt;L'elemento propertyStore &gt; specifica un set di una o più proprietà usate da questa libreria. Questo elemento è facoltativo e non ha attributi.

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

&lt;L'elemento propertyStore &gt; può avere uno o più elementi figlio di &lt; &gt; proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Schema di descrizione della libreria](library-schema-entry.md)
</dt> <dt>

[Schema di descrizione del connettore di ricerca](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
