---
description: Criteri dei metadati della foto per la proprietà System.Photo.CameraManufacturer.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: Criteri dei metadati delle foto di System.Photo.CameraManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37744420babedf6b398cdf3ab9007c3895c09d33b9254221b5ba4760ab917a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087087"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.Photo.CameraManufacturer

Criteri dei metadati della foto per [la proprietà System.Photo.CameraManufacturer.](../properties/props-system-photo-cameramanufacturer.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ CameraManufacturer

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

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=271} | ascii       |
| 2     | /xmp/tiff:Make         | unicode     |
| 3     | /xmp/tiff:make         | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=271} | ascii       |
| 2     | /xmp/tiff:Make         | unicode     |
| 3     | /xmp/tiff:make         | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=271} |
| 2     | /xmp/tiff:Make         |
| 3     | /xmp/tiff:make         |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso               | Formato disco |
|-------|--------------------|-------------|
| 1     | /ifd/{ushort=271}  | ascii       |
| 2     | /ifd/xmp/tiff:Make | unicode     |
| 3     | /ifd/xmp/tiff:make | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso               | Formato disco |
|-------|--------------------|-------------|
| 1     | /ifd/{ushort=271}  | ascii       |
| 2     | /ifd/xmp/tiff:Make | unicode     |
| 3     | /ifd/xmp/tiff:make | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso               |
|-------|--------------------|
| 1     | /ifd/{ushort=271}  |
| 2     | /ifd/xmp/tiff:Make |
| 3     | /ifd/xmp/tiff:make |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
