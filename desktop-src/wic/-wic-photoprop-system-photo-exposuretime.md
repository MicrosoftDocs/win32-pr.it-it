---
description: Criteri per i metadati delle foto per la proprietà System. Photo. ExposureTime.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: Criteri per i metadati delle foto di System. Photo. ExposureTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314455"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. ExposureTime

Criteri per i metadati delle foto per la proprietà [System. Photo. ExposureTime](../properties/props-system-photo-exposuretime.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ ExposureTime

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. Photo. ExposureTimeNumerator e System. Photo. ExposureTimeDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 33434} |             |
| 2     | /XMP/EXIF: ExposureTime        |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 33434} |             |
| 2     | /XMP/EXIF: ExposureTime        |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 33434} |
| 2     | /XMP/EXIF: ExposureTime        |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 33434}   |             |
| 2     | /IFD/XMP/EXIF: ExposureTime |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 33434}   |             |
| 2     | /IFD/XMP/EXIF: ExposureTime |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{ushort = 33434}   |
| 2     | /IFD/XMP/EXIF: ExposureTime |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. ExposureTime](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
