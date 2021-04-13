---
description: Criteri per i metadati delle foto per la proprietà System. Photo. DigitalZoom.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Criteri per i metadati delle foto di System. Photo. DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347426"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. DigitalZoom

Criteri per i metadati delle foto per la proprietà [System. Photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ DigitalZoom

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. Photo. DigitalZoomNumerator e System. Photo. DigitalZoomDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41988} |
| 2     | /xmp/exif:digitalzoomratio    |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                           |
|-------|--------------------------------|
| 1     | /IFD/EXIF/{ushort = 41988}       |
| 2     | /ifd/xmp/exif:digitalzoomratio |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
