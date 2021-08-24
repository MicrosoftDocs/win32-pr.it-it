---
description: Criteri dei metadati delle foto per la proprietà System.GPS.MeasureMode.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Criteri dei metadati delle foto system.GPS.MeasureMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827cd278a71b23934fb0475e78d98b25a9f2b72d413b70f9abc60ba3dbe2c3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882321"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a>Criteri dei metadati delle foto system.GPS.MeasureMode

Criteri dei metadati delle foto per [la proprietà System.GPS.MeasureMode.](../properties/props-system-gps-measuremode.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ MeasureMode

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



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=10} |
| 2     | /xmp/exif:gpsmeasuremode  |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                         |
|-------|------------------------------|
| 1     | /ifd/gps/{ushort=10}         |
| 2     | /ifd/xmp/exif:gpsmeasuremode |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.MeasureMode](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
