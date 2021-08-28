---
description: L'elemento templateInfo è un contenitore per l'elemento folderType, che specifica un tipo di cartella per visualizzare i risultati di una &lt; &gt; query su questa libreria. Questo elemento è facoltativo e non ha attributi.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Elemento templateInfo (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f55fec64bf7418eef8e70c4cf8fa1ee47006c5f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885527"
---
# <a name="templateinfo-element-library-schema"></a>Elemento templateInfo (schema della libreria)

L'elemento templateInfo è un contenitore per l'elemento &lt; &gt; [folderType,](schema-library-foldertype.md) che specifica un tipo di cartella per visualizzare i risultati di una query su questa libreria. Questo elemento è facoltativo e non ha attributi.

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

 

 
