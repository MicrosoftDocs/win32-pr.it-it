---
description: Criteri dei metadati delle foto per la proprietà System.Photo.CameraModel.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Criteri metadati foto System.Photo.CameraModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e205d4d886d050e45b958f2ba0f06c6411584c4a96a717378f243e5d1dd4fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882051"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a>Criteri metadati foto System.Photo.CameraModel

Criteri dei metadati delle foto per [la proprietà System.Photo.CameraModel.](../properties/props-system-photo-cameramodel.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ CameraModel

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
| 1     | /app1/ifd/{ushort=272} | ascii       |
| 2     | /xmp/tiff:Model        | unicode     |
| 3     | /xmp/tiff:model        | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=272} | ascii       |
| 2     | /xmp/tiff:Model        | unicode     |
| 3     | /xmp/tiff:model        | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=272} |
| 2     | /xmp/tiff:Model        |
| 3     | /xmp/tiff:model        |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                | Formato disco |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=272}   | ascii       |
| 2     | /ifd/xmp/tiff:Model | unicode     |
| 3     | /ifd/xmp/tiff:model | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                | Formato disco |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=272}   | ascii       |
| 2     | /ifd/xmp/tiff:Model | unicode     |
| 3     | /ifd/xmp/tiff:model | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                |
|-------|---------------------|
| 1     | /ifd/{ushort=272}   |
| 2     | /ifd/xmp/tiff:Model |
| 3     | /ifd/xmp/tiff:model |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
