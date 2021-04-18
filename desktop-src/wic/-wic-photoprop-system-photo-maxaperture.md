---
description: Criteri per i metadati delle foto per la proprietà System. Photo. MaxAperture.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: Criteri per i metadati delle foto di System. Photo. MaxAperture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314446"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. MaxAperture

Criteri per i metadati delle foto per la proprietà [System. Photo. MaxAperture](../properties/props-system-photo-maxaperture.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ MaxAperture

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="input-type"></a>Tipo di input

Double

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. Photo. MaxApertureNumerator e System. Photo. MaxApertureDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37381} |             |
| 2     | /xmp/exif:MaxApertureValue    |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37381} |             |
| 2     | /xmp/exif:MaxApertureValue    |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37381} |
| 2     | /xmp/exif:maxaperturevalue    |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37381}       |             |
| 2     | /ifd/xmp/exif:MaxApertureValue |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37381}       |             |
| 2     | /ifd/xmp/exif:MaxApertureValue |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                           |
|-------|--------------------------------|
| 1     | /IFD/EXIF/{ushort = 37381}       |
| 2     | /ifd/xmp/exif:maxaperturevalue |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. MaxAperture](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
