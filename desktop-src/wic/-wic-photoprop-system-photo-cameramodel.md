---
description: Criteri per i metadati delle foto per la proprietà System. Photo. CameraModel.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Criteri per i metadati delle foto di System. Photo. CameraModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884649"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. CameraModel

Criteri per i metadati delle foto per la proprietà [System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ CameraModel

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 272} | ascii       |
| 2     | /XMP/TIFF: modello        | unicode     |
| 3     | /XMP/TIFF: modello        | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 272} | ascii       |
| 2     | /XMP/TIFF: modello        | unicode     |
| 3     | /XMP/TIFF: modello        | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                   |
|-------|------------------------|
| 1     | /App1/IFD/{ushort = 272} |
| 2     | /XMP/TIFF: modello        |
| 3     | /XMP/TIFF: modello        |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                | Formato disco |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 272}   | ascii       |
| 2     | /IFD/XMP/TIFF: modello | unicode     |
| 3     | /IFD/XMP/TIFF: modello | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                | Formato disco |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 272}   | ascii       |
| 2     | /IFD/XMP/TIFF: modello | unicode     |
| 3     | /IFD/XMP/TIFF: modello | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                |
|-------|---------------------|
| 1     | /IFD/{ushort = 272}   |
| 2     | /IFD/XMP/TIFF: modello |
| 3     | /IFD/XMP/TIFF: modello |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
