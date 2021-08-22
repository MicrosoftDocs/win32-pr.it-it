---
description: Criteri dei metadati delle foto per la proprietà System.Photo.Dispeed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Criteri dei metadati delle foto system.photo.Dispeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad11550a19cd043fd5d182b2cf508aec3e26c64a0dc2ee1d1c24576ebf18f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710100"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a>Criteri dei metadati delle foto system.photo.Dispeed

Criteri dei metadati delle foto [per la proprietà System.Photo.Dispeed.](../properties/props-system-photo-shutterspeed.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ PhotoSpeed

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System.Photo.ConspeedNumerator e System.Photo.TaliSpeedDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37377} |             |
| 2     | /xmp/exif:PiùSpeedValue   |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37377} |             |
| 2     | /xmp/exif:PiùSpeedValue   |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37377} |
| 2     | /xmp/exif:più valori   |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                            | Formato disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37377}        |             |
| 2     | /ifd/xmp/exif:PiùSpeedValue |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                            | Formato disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37377}        |             |
| 2     | /ifd/xmp/exif:PiùSpeedValue |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                            |
|-------|---------------------------------|
| 1     | /ifd/exif/{ushort=37377}        |
| 2     | /ifd/xmp/exif:piùspeedvalue |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.Conspeed](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
