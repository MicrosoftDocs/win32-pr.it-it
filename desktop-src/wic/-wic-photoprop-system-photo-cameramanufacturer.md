---
description: Criteri per i metadati delle foto per la proprietà System. Photo. CameraManufacturer.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: Criteri per i metadati delle foto di System. Photo. CameraManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317248"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. CameraManufacturer

Criteri per i metadati delle foto per la proprietà [System. Photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ CameraManufacturer

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
| 1     | /App1/IFD/{ushort = 271} | ascii       |
| 2     | /XMP/TIFF: make         | unicode     |
| 3     | /XMP/TIFF: make         | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 271} | ascii       |
| 2     | /XMP/TIFF: make         | unicode     |
| 3     | /XMP/TIFF: make         | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                   |
|-------|------------------------|
| 1     | /App1/IFD/{ushort = 271} |
| 2     | /XMP/TIFF: make         |
| 3     | /XMP/TIFF: make         |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso               | Formato disco |
|-------|--------------------|-------------|
| 1     | /IFD/{ushort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF: make | unicode     |
| 3     | /IFD/XMP/TIFF: make | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso               | Formato disco |
|-------|--------------------|-------------|
| 1     | /IFD/{ushort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF: make | unicode     |
| 3     | /IFD/XMP/TIFF: make | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso               |
|-------|--------------------|
| 1     | /IFD/{ushort = 271}  |
| 2     | /IFD/XMP/TIFF: make |
| 3     | /IFD/XMP/TIFF: make |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
