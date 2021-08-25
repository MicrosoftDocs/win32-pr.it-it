---
description: L'elemento è un contenitore per l'elemento folderType, che specifica un tipo di cartella per la visualizzazione dei risultati di <templateInfo> una query su questa libreria. Questo elemento è facoltativo e non ha attributi.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Elemento templateInfo (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda0c42e71db2e47335371b51d9dc819620e6b28dfac63ee9c0e2a640ccab0b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942091"
---
# <a name="templateinfo-element-library-schema"></a>Elemento templateInfo (schema della libreria)

L'elemento è un contenitore per l'elemento folderType, che specifica un tipo di cartella per la visualizzazione dei risultati di <templateInfo> una query su questa libreria. [](schema-library-foldertype.md) Questo elemento è facoltativo e non ha attributi.

## <a name="syntax"></a>Sintassi

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                               | Elementi figlio                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Elemento libraryDescription (schema della libreria)](schema-librarydescription.md) | [Elemento folderType (schema della libreria)](schema-library-foldertype.md)       |
|                                                                              | [Elemento propertyStore (schema della libreria)](schema-library-propertystore.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Schema di descrizione della libreria](library-schema-entry.md)
</dt> <dt>

[Schema di descrizione del connettore di ricerca](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
