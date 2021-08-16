---
description: Criteri dei metadati delle foto per la proprietà System.GPS.ProcessingMethod.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: Criteri dei metadati delle foto di System.GPS.ProcessingMethod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800515d3a7870fa2dc9b5a6ec8c19178889482fa820f66d7d98e8e3ff09870f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931741"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.GPS.ProcessingMethod

Criteri dei metadati delle foto per [la proprietà System.GPS.ProcessingMethod.](../properties/props-system-gps-processingmethod.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ ProcessingMethod

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

VT \_ LPWSTR è preferibile, ma viene accettato anche \_ VT LPSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policies"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/gps/{ushort=27}     |
| 2     | /xmp/exif:gpsprocessingmethod |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                              | Formato disco |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | unicode     |
| 2     | /ifd/gps/{ushort=27}              |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                              | Formato disco |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | unicode     |
| 2     | /ifd/gps/{ushort=27}              |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                              |
|-------|-----------------------------------|
| 1     | /ifd/xmp/exif:gpsprocessingmethod |
| 2     | /ifd/gps/{ushort=27}              |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.ProcessingMethod](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
