---
description: L' <templateInfo> elemento è un contenitore per l'elemento FolderType, che specifica un tipo di cartella per la visualizzazione dei risultati di una query su questa libreria. Questo elemento è facoltativo e non ha attributi.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Elemento templateInfo (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527306"
---
# <a name="templateinfo-element-library-schema"></a>Elemento templateInfo (schema della libreria)

L' <templateInfo> elemento è un contenitore per l'elemento [FolderType](schema-library-foldertype.md) , che specifica un tipo di cartella per la visualizzazione dei risultati di una query su questa libreria. Questo elemento è facoltativo e non ha attributi.

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

[Schema Descrizione libreria](library-schema-entry.md)
</dt> <dt>

[Cerca nello schema di descrizione del connettore](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
