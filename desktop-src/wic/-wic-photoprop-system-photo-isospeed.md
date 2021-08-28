---
description: Criteri dei metadati delle foto per la proprietà System.Photo.ISOSpeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Criteri metadati foto System.Photo.ISOSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6612bffdeaafb69ea1b1122a1d75c00214d366e9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881633"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a>Criteri metadati foto System.Photo.ISOSpeed

Criteri dei metadati delle foto [per la proprietà System.Photo.ISOSpeed.](../properties/props-system-photo-focallengthinfilm.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ ISOSpeed

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

Interfaccia utente \_ VT2

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                    | Formato disco |
|-------|-----------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34855}           | ushort      |
| 2     | /xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | unicode     |
| 3     | /xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                    | Formato disco |
|-------|-----------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34855}           | ushort      |
| 2     | /xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | unicode     |
| 3     | /xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                    |
|-------|-----------------------------------------|
| 1     | /app1/ifd/exif/{ushort=34855}           |
| 2     | /xmp/ &lt; xmpseq &gt; exif:isospeedratings |
| 3     | /xmp/exif:isospeed                      |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                        | Formato disco |
|-------|---------------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34855}                    | ushort      |
| 2     | /ifd/xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                        | Formato disco |
|-------|---------------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34855}                    | ushort      |
| 2     | /ifd/xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                        |
|-------|---------------------------------------------|
| 1     | /ifd/exif/{ushort=34855}                    |
| 2     | /ifd/xmp/ &lt; xmpseq &gt; exif:isospeedratings |
| 3     | /ifd/xmp/exif:isospeed                      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.ISOSpeed](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
