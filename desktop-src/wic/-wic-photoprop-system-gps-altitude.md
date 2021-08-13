---
description: Criteri dei metadati delle foto per la proprietà System.GPS.Altitude.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Criteri dei metadati delle foto di System.GPS.Altitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a9209bfb0bbc1a4c6f95ce4a995d32d3f532c293dd2295c335eea61c22df89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442001"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.GPS.Altitude

Criteri dei metadati delle foto per [la proprietà System.GPS.Altitude.](../properties/props-system-gps-altitude.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ Altitude

### <a name="description"></a>Descrizione

L'altitudine è indicata come valore assoluto a cui si fa riferimento in metri.

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ R8

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore può essere scritto in System.GPS.Altitude.Numerator e System.GPS.Altitude.Denominator. Non può essere scritto direttamente. I percorsi di scrittura nelle tabelle seguenti indicano dove è possibile salvare il valore quando viene generato, non quando viene scritto direttamente. Quando il valore viene letto, i valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=6} |
| 2     | /xmp/exif:gpsaltitude    |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                      |     |
|-------|---------------------------|-----|
| 1     | /ifd/gps/{ushort=6}       |     |
| 2     | /ifd/xmp/exif:gpsaltitude |     |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.Altitude](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
