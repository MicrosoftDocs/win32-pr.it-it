---
description: Criteri per i metadati delle foto per la proprietà System. Photo. luminosità.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Criteri per i metadati delle foto System. Photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968332"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a>Criteri per i metadati delle foto System. Photo. Brightness

Criteri per i metadati delle foto per la proprietà [System. Photo. luminosità](../properties/props-system-photo-aperture.md) .

### <a name="pkey"></a>PKEY

PKEY \_ \_ luminosità foto

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="input-type"></a>Tipo di input

Double

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. Photo. ApertureNumerator e System. Photo. ApertureDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37379} |
| 2     | /xmp/exif:brightnessvalue     |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /IFD/EXIF/{ushort = 37379}      |
| 2     | /ifd/xmp/exif:brightnessvalue |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. Brightness](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
