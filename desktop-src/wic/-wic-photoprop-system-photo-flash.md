---
description: Criteri per i metadati delle foto per la proprietà System. Photo. Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Criteri per i metadati delle foto di System. Photo. Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314454"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. Flash

Criteri per i metadati delle foto per la proprietà [System. Photo. Flash](../properties/props-system-photo-exposuretime.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ Flash

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ Ui1 (se lo schema di origine è XMP) o VT \_ UI2 (se lo schema di origine è EXIF)

\\lang1036

### <a name="input-type"></a>Tipo di input

VT \_ Ui1, VTUI2, VT \_ UI4

\\lang1033

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37385}    | ushort      |
| 2     | /XMP/ <xmpstruct> EXIF: Flash |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37385}    | ushort      |
| 2     | /XMP/ <xmpstruct> EXIF: Flash |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                             |
|-------|----------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37385}    |
| 2     | /XMP/ <xmpstruct> EXIF: Flash |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                 | Formato disco |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37385}             | ushort      |
| 2     | /IFD/XMP/ <xmpstruct> EXIF: Flash |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                 | Formato disco |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37385}             | ushort      |
| 2     | /IFD/XMP/ <xmpstruct> EXIF: Flash |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                 |
|-------|--------------------------------------|
| 1     | /IFD/EXIF/{ushort = 37385}             |
| 2     | /IFD/XMP/ <xmpstruct> EXIF: Flash |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
