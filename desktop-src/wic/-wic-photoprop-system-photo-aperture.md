---
description: Criteri per i metadati delle foto per la proprietà System. Photo. aperture.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: Criteri per i metadati di Photo System. Photo. aperture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317251"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a>Criteri per i metadati di Photo System. Photo. aperture

Criteri per i metadati delle foto per la proprietà [System. Photo. aperture](../properties/props-system-photo-aperture.md) .

### <a name="pkey"></a>PKEY

\_Apertura foto \_ pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. Photo. ApertureNumerator e System. Photo. ApertureDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37378} |             |
| 2     | /xmp/exif:ApertureValue       |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37378} |             |
| 2     | /xmp/exif:ApertureValue       |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37378} |
| 2     | /xmp/exif:aperturevalue       |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                        | Formato disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37378}    |             |
| 2     | /ifd/xmp/exif:ApertureValue |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                        | Formato disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37378}    |             |
| 2     | /ifd/xmp/exif:ApertureValue |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                        |
|-------|-----------------------------|
| 1     | /IFD/EXIF/{ushort = 37378}    |
| 2     | /ifd/xmp/exif:aperturevalue |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. aperture](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
