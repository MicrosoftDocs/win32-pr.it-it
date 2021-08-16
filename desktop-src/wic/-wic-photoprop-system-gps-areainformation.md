---
description: Criteri dei metadati delle foto per la proprietà System.GPS.AreaInformation.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Criteri dei metadati foto system.GPS.AreaInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4eee2cf4234902049241c833d1077814f5daf88187323c43bc1cb00f6f44aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205522"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a>Criteri dei metadati foto system.GPS.AreaInformation

Criteri dei metadati delle foto per [la proprietà System.GPS.AreaInformation.](../properties/props-system-gps-areainformation.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ GPS \_ AreaInformation

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



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort=28}    |
| 2     | /xmp/exif:GPSAreaInformation |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort=28}             |
| 2     | /ifd/xmp/exif:GPSAreaInformation |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.AreaInformation](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
