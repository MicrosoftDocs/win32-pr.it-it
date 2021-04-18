---
description: Criteri per i metadati delle foto per la proprietà System. Photo. FocalLength.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: Criteri per i metadati delle foto di System. Photo. FocalLength
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314883"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. FocalLength

Criteri per i metadati delle foto per la proprietà [System. Photo. focalLength](../properties/props-system-photo-focallength.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ focalLength

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. Photo. FocalLengthNumerator e System. Photo. FocalLengthDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37386} |             |
| 2     | /XMP/EXIF: FocalLength         |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37386} |             |
| 2     | /XMP/EXIF: FocalLength         |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37386} |
| 2     | /XMP/EXIF: focalLength         |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37386}  |             |
| 2     | /IFD/XMP/EXIF: FocalLength |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37386}  |             |
| 2     | /IFD/XMP/EXIF: FocalLength |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{ushort = 37386}  |
| 2     | /IFD/XMP/EXIF: focalLength |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. FocalLength](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
