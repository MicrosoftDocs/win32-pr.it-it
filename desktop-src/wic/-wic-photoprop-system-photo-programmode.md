---
description: Criteri per i metadati delle foto per la proprietà System. Photo. ProgramMode.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: Criteri per i metadati delle foto di System. Photo. ProgramMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968116"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. ProgramMode

Criteri per i metadati delle foto per la proprietà [System. Photo. ProgramMode](../properties/props-system-photo-programmode.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ ProgramMode

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_UI4 VT

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 34850} | ushort      |
| 2     | /XMP/EXIF: ExposureProgram     | unicode     |
| 3     | /xmp/exif:ProgramMode         | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 34850} | ushort      |
| 2     | /XMP/EXIF: ExposureProgram     | unicode     |
| 3     | /xmp/exif:ProgramMode         | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 34850} |
| 2     | /XMP/EXIF: ExposureProgram     |
| 3     | /xmp/exif:programmode         |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 34850}      | ushort      |
| 2     | /IFD/XMP/EXIF: ExposureProgram | unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 34850}      | ushort      |
| 2     | /IFD/XMP/EXIF: ExposureProgram | unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /IFD/EXIF/{ushort = 34850}      |
| 2     | /IFD/XMP/EXIF: ExposureProgram |
| 3     | /ifd/xmp/exif:programmode     |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
