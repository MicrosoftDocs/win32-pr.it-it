---
description: Criteri dei metadati della foto per la proprietà System.Photo.MakerNote.
ms.assetid: e1018bc6-3fd2-4212-afee-6811bfe99f14
title: Criteri dei metadati delle foto di System.Photo.MakerNote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c6e6cc89f5e1353d460b003b718c768f11896547e36b86807edeb6099aef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032558"
---
# <a name="systemphotomakernote-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.Photo.MakerNote

Criteri dei metadati della foto per [la proprietà System.Photo.MakerNote.](../properties/props-system-photo-makernote.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ MakerNote

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

\_ \| VTUI1 VETTORE VT

### <a name="input-type"></a>Tipo di input

Buffer

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37500} |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37500} |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37500} |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=37500} |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=37500} |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=37500} |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.MakerNote](../properties/props-system-photo-makernote.md)
</dt> </dl>

 

 
