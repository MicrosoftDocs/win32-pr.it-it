---
description: Criteri dei metadati delle foto per la proprietà System.Photo.Brightness.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Criteri dei metadati delle foto system.Photo.Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78549d86d50f9b48359932698b02c827bd454a439476f2dc82627e4aab21d25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882061"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a>Criteri dei metadati delle foto system.Photo.Brightness

Criteri dei metadati delle foto per [la proprietà System.Photo.Brightness.](../properties/props-system-photo-aperture.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ Brightness

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="input-type"></a>Tipo di input

Double

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System.Photo.ApertureNumerator e System.Photo.ApertureDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37379} |
| 2     | /xmp/exif:luminositàvalore     |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /ifd/exif/{ushort=37379}      |
| 2     | /ifd/xmp/exif:luminositàvalore |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.Brightness](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
