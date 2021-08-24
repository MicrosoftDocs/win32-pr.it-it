---
description: <iconReference>L'elemento specifica un'icona personalizzata per questa libreria. Questo elemento è facoltativo e non dispone di attributi o elementi figlio.
title: Elemento iconReference (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 84e200fa4969dc376661bd32851296d80c74120939afc995754cb2937ea04be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820231"
---
# <a name="iconreference-element-library-schema"></a>Elemento iconReference (schema della libreria)

<iconReference>L'elemento specifica un'icona personalizzata per questa libreria. Questo elemento è facoltativo e non dispone di attributi o elementi figlio.

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

Il riferimento all'icona deve essere specificato in un formato adatto per la [**funzione PathParseIconLocation.**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) Ad esempio: `ModuleFileName,IconResourceIndex`.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elemento folderType (schema della libreria)](schema-library-foldertype.md)
</dt> <dt>

[Elemento isLibraryPinned (schema della libreria)](schema-library-islibrarypinned.md)
</dt> <dt>

[Elemento libraryDescription (schema della libreria)](schema-librarydescription.md)
</dt> <dt>

[Elemento name (schema della libreria)](schema-library-name.md)
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

[Elemento version (schema della libreria)](schema-library-version.md)
</dt> </dl>

 

 



