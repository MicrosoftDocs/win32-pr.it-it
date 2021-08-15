---
description: Criteri dei metadati delle foto per la proprietà System.Photo.LightSource.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Criteri dei metadati delle foto System.Photo.LightSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195d165a6a929c8e0b4bf2dd165a5f22068a8b75e8ea4dfcddb5b8979900b035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204723"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>Criteri dei metadati delle foto System.Photo.LightSource

Criteri dei metadati delle foto per [la proprietà System.Photo.LightSource.](../properties/props-system-photo-lightsource.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ LightSource

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ UI4

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37384} | ushort      |
| 2     | /xmp/exif:LightSource         | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37384} | ushort      |
| 2     | /xmp/exif:LightSource         | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37384} |
| 2     | /xmp/exif:lightsource         |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=37384}  | ushort      |
| 2     | /ifd/xmp/exif:LightSource | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=37384}  | ushort      |
| 2     | /ifd/xmp/exif:LightSource | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=37384}  |
| 2     | /ifd/xmp/exif:lightsource |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.LightSource](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
