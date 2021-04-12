---
description: Criteri per i metadati delle foto per la proprietà System. Photo. ISOSpeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Criteri per i metadati delle foto di System. Photo. ISOSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346601"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. ISOSpeed

Criteri per i metadati delle foto per la proprietà [System. Photo. ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ ISOSpeed

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_UI2 VT

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                    | Formato disco |
|-------|-----------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 34855}           | ushort      |
| 2     | /XMP/ <xmpseq> EXIF: ISOSpeedRatings | unicode     |
| 3     | /xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                    | Formato disco |
|-------|-----------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 34855}           | ushort      |
| 2     | /XMP/ <xmpseq> EXIF: ISOSpeedRatings | unicode     |
| 3     | /xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                    |
|-------|-----------------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 34855}           |
| 2     | /XMP/ <xmpseq> EXIF: ISOSpeedRatings |
| 3     | /xmp/exif:isospeed                      |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                        | Formato disco |
|-------|---------------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 34855}                    | ushort      |
| 2     | /IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings | unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                        | Formato disco |
|-------|---------------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 34855}                    | ushort      |
| 2     | /IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings | unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                        |
|-------|---------------------------------------------|
| 1     | /IFD/EXIF/{ushort = 34855}                    |
| 2     | /IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings |
| 3     | /ifd/xmp/exif:isospeed                      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. ISOSpeed](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
