---
description: <folderType>L'elemento specifica un GUID per il tipo di cartella. Questo elemento è obbligatorio se <templateInfo> l'elemento esiste; in caso contrario, è facoltativo. Questo elemento non ha attributi e nessun elemento figlio.
title: Elemento folderType (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8d35f09a10cc88ae3873a507b6fa7000812503890240ce0b808ffecc84f23fd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883951"
---
# <a name="foldertype-element-library-schema"></a>Elemento folderType (schema della libreria)

<folderType>L'elemento specifica un GUID per il tipo di cartella. Questo elemento è obbligatorio se <templateInfo> l'elemento esiste; in caso contrario, è facoltativo. Questo elemento non ha attributi e nessun elemento figlio.

## <a name="syntax"></a>Sintassi


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                           | Elementi figlio |
|--------------------------------------------------------------------------|----------------|
| [Elemento templateInfo (schema della libreria)](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a>Commenti

L'impostazione di un tipo di cartella determina le colonne e i dettagli visualizzati in Windows Explorer per impostazione predefinita. Gli identificatori dei tipi di cartella ([**FOLDERTYPEID**](foldertypeid.md)) sono GUID definiti in Shlguid.h. Nella tabella seguente sono elencati i GUID dei tipi di cartella comuni.



| Tipo di cartella      | GUID                                   |
|------------------|----------------------------------------|
| Libreria generica  | {5f4eab9a-6833-4f61-899d-31cf46979d49} |
| Librerie degli utenti  | {C4D98F09-6124-4fe0-9942-826416082DA9} |
| Cartella Documenti | {7D49D726-3C21-4F05-99AA-FDC2C9474656} |
| Cartella Immagini  | {B3690E58-E961-423B-B687-386EBFD83239} |
| Cartella Video    | {5fa96407-7e77-483c-ac93-691d05850de8} |
| Cartella Games     | {b689b0d0-76d3-4cbb-87f7-585d0e0ce070} |
| Musica Cartella     | {94d6ddcc-4a68-4175-a374-bd584a510b78} |
| Contatti         | {DE2B70EC-9BF7-4A93-BD3D-243F7881D492} |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elemento iconReference (schema della libreria)](schema-library-iconreference.md)
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

 

 



