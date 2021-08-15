---
description: Criteri dei metadati delle foto per la proprietà System.GPS.DestBearingRef.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: Criteri metadati foto System.GPS.DestBearingRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ee4b984d0a759769b80be76b53499690673c7ec630c759aa0371b53ea9368f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087852"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a>Criteri metadati foto System.GPS.DestBearingRef

Criteri dei metadati delle foto per [la proprietà System.GPS.DestBearingRef.](../properties/props-system-gps-destbearingref.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ GPS \_ DestBearingRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policies"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                        | Formato disco |
|-------|-----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                        | Formato disco |
|-------|-----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                        |
|-------|-----------------------------|
| 1     | /app1/ifd/gps/{ushort=23}   |
| 2     | /xmp/exif:gpsdestbearingref |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                            | Formato disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/gps/{ushort=23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                            | Formato disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/gps/{ushort=23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| order | path                            |
|-------|---------------------------------|
| 1     | /ifd/gps/{ushort=23}            |
| 2     | /ifd/xmp/exif:gpsdestbearingref |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.DestBearingRef](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
