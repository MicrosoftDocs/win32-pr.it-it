---
description: Criteri per i metadati delle foto per la proprietà System. Photo. EXIFVersion.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Criteri per i metadati delle foto di System. Photo. EXIFVersion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233332"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. EXIFVersion

Criteri per i metadati delle foto per la proprietà [System. Photo. EXIFVersion](../properties/props-system-photo-exifversion.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ EXIFVersion

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



| JSON | Percorso                          | Formato disco   |
|-------|-------------------------------|---------------|
| 1     | /App1/IFD/EXIF/{ushort = 36864} | \_versione Exif |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco   |
|-------|-------------------------------|---------------|
| 1     | /App1/IFD/EXIF/{ushort = 36864} | \_versione Exif |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 36864} |
| 2     | /xmp/exif:ExifVersion         |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco   |
|-------|---------------------------|---------------|
| 1     | /IFD/EXIF/{ushort = 36864}  | \_versione Exif |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco   |
|-------|---------------------------|---------------|
| 1     | /IFD/EXIF/{ushort = 36864}  | \_versione Exif |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{ushort = 36864}  |
| 2     | /ifd/xmp/exif:ExifVersion |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. EXIFVersion](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
