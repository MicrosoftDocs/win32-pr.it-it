---
description: Criteri dei metadati delle foto per la proprietà System.GPS.SpeedRef.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Criteri dei metadati delle foto System.GPS.SpeedRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c7b60a0c8decaf5ecc30f9017a0aadc61bb9fe4814240fb7ab2e022d6a2873f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549491"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a>Criteri dei metadati delle foto System.GPS.SpeedRef

Criteri dei metadati delle foto per [la proprietà System.GPS.SpeedRef.](../properties/props-system-gps-speedref.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ GPS \_ SpeedRef

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
| 1     | /app1/ifd/gps/{ushort=12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      | Formato del disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=12} |             |
| 2     | /xmp/exif:gpsspeedref     |             |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      |         |
|-------|---------------------------|---------|
| 1     | /ifd/gps/{ushort=12}      | ascii   |
| 2     | /ifd/xmp/exif:GPSSpeedRef | unicode |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=12}      | ascii       |
| 2     | /ifd/xmp/exif:GPSSpeedRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /ifd/gps/{ushort=12}      |
| 2     | /ifd/xmp/exif:gpsspeedref |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.SpeedRef](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
