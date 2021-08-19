---
description: Criteri dei metadati delle foto per la proprietà System.GPS.ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Criteri dei metadati delle foto system.GPS.ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e735f91133d4ec473537f063e30d2d48f801a99f8f6bc80fa228b98a9bd95437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667898"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>Criteri dei metadati delle foto system.GPS.ImgDirectionRef

Criteri dei metadati delle foto per [la proprietà System.GPS.ImgDirectionRef.](../properties/props-system-gps-imgdirectionref.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS. ImgDirectionRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

VT \_ LPWSTR è preferibile, ma viene accettato anche \_ VT LPSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policies"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort=16}    |
| 2     | /xmp/exif:gpsimgdirectionref |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort=16}             |
| 2     | /ifd/xmp/exif:gpsimgdirectionref |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
