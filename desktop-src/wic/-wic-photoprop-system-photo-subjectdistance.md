---
description: Criteri dei metadati delle foto per la proprietà System.Photo.SubjectDistance.
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: Criteri metadati foto System.Photo.SubjectDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ec1868b1e33c4bcaaaea9a9203cc73733646cc82dade52c86b0c8caec4a704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964770"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a>Criteri metadati foto System.Photo.SubjectDistance

Criteri dei metadati delle foto [per la proprietà System.Photo.SubjectDistance.](../properties/props-system-photo-subjectdistance.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ SubjectDistance

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System.Photo.SubjectDistanceNumerator e System.Photo.SubjectDistanceDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37382} |             |
| 2     | /xmp/exif:SubjectDistance     |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37382} |             |
| 2     | /xmp/exif:SubjectDistance     |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37382} |
| 2     | /xmp/exif:subjectdistance     |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37382}      |             |
| 2     | /ifd/xmp/exif:SubjectDistance |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37382}      |             |
| 2     | /ifd/xmp/exif:SubjectDistance |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /ifd/exif/{ushort=37382}      |
| 2     | /ifd/xmp/exif:subjectdistance |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.SubjectDistance](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
