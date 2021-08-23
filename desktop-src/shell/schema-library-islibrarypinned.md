---
description: <isLibraryPinned>L'elemento specifica se questa libreria è bloccata nel riquadro di spostamento in Windows Explorer. Questo elemento è facoltativo e non ha elementi figlio e nessun attributo.
title: Elemento isLibraryPinned (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: AD8307E5-5676-4d43-8FEE-695F168F677D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8b5fe37b2a9b31708c1b6a49bd22745b37af8fa8ec21b0b424b7c6da3baaae53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592861"
---
# <a name="islibrarypinned-element-library-schema"></a>Elemento isLibraryPinned (schema della libreria)

<isLibraryPinned>L'elemento specifica se questa libreria è bloccata nel riquadro di spostamento in Windows Explorer. Questo elemento è facoltativo e non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- isLibraryPinned -->
    <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                               | Elementi figlio |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (schema della libreria)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Commenti

Se true, la libreria viene aggiunta al riquadro di Windows Explorer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elemento libraryDescription (schema della libreria)](schema-librarydescription.md)
</dt> <dt>

[Elemento searchConnectorDescription (schema della libreria)](schema-library-searchconnectordescription.md)
</dt> </dl>

 

 



