---
description: L' <iconReference> elemento specifica un'icona personalizzata per questa libreria. Questo elemento è facoltativo e non dispone di attributi o elementi figlio.
title: Elemento iconReference (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f307ecd4fa523cc28881164869dca3329dfd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994149"
---
# <a name="iconreference-element-library-schema"></a>Elemento iconReference (schema della libreria)

L' <iconReference> elemento specifica un'icona personalizzata per questa libreria. Questo elemento è facoltativo e non dispone di attributi o elementi figlio.

## <a name="syntax"></a>Sintassi


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                               | Elementi figlio |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (schema della libreria)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Commenti

Il riferimento all'icona deve essere specificato in un formato appropriato per la funzione [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) . Ad esempio: `ModuleFileName,IconResourceIndex`.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elemento folderType (schema della libreria)](schema-library-foldertype.md)
</dt> <dt>

[Elemento isLibraryPinned (schema della libreria)](schema-library-islibrarypinned.md)
</dt> <dt>

[Elemento libraryDescription (schema della libreria)](schema-librarydescription.md)
</dt> <dt>

[Elemento Name (schema della libreria)](schema-library-name.md)
</dt> <dt>

[Elemento ownerSID (schema della libreria)](schema-library-ownersid.md)
</dt> <dt>

[Elemento propertyStore (schema della libreria)](schema-library-propertystore.md)
</dt> <dt>

[Elemento searchConnectorDescription (schema della libreria)](schema-library-searchconnectordescription.md)
</dt> <dt>

[Elemento searchConnectorDescriptionList (schema della libreria)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[Elemento templateInfo (schema della libreria)](schema-library-templateinfo.md)
</dt> <dt>

[Elemento Version (schema della libreria)](schema-library-version.md)
</dt> </dl>

 

 



