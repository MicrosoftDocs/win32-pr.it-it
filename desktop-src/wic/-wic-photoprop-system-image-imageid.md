---
description: Criteri per i metadati delle foto per la proprietà System. image. ImageID.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Criteri per i metadati delle foto di System. image. ImageID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529269"
---
# <a name="systemimageimageid-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. image. ImageID

Criteri per i metadati delle foto per la proprietà [System. image. ImageId](../properties/props-system-image-imageid.md) .

### <a name="pkey"></a>PKEY

Immagine di PKEY \_ \_ ImageId

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 42016} | ascii       |
| 2     | /XMP/EXIF: ImageUniqueID       | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 42016} | ascii       |
| 2     | /XMP/EXIF: ImageUniqueID       | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 42016} |
| 2     | /XMP/EXIF: ImageUniqueID       |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                        | Formato disco |
|-------|-----------------------------|-------------|
|       | /IFD/EXIF/{ushort = 42016}    | ascii       |
|       | /IFD/XMP/EXIF: ImageUniqueID | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                        | Formato disco |
|-------|-----------------------------|-------------|
|       | /IFD/EXIF/{ushort = 42016}    | ascii       |
|       | /IFD/XMP/EXIF: ImageUniqueID | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                        |
|-------|-----------------------------|
|       | /IFD/EXIF/{ushort = 42016}    |
|       | /IFD/XMP/EXIF: ImageUniqueID |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. image. ImageID](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
