---
description: Criteri dei metadati delle foto per la proprietà System.Image.VerticalResolution.
ms.assetid: a58b7463-3572-4ca8-8299-93d92d2f06fb
title: Criteri metadati foto System.Image.VerticalResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9962a00be34d227756d295e992174d6e80b6d058fc32af29ad9cde58a04ed07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710284"
---
# <a name="systemimageverticalresolution-photo-metadata-policy"></a>Criteri metadati foto System.Image.VerticalResolution

Criteri dei metadati delle foto per [la proprietà System.Image.VerticalResolution.](../properties/props-system-image-verticalresolution.md)

### <a name="pkey"></a>Chiave PKEY

Immagine PKEY \_ \_ VerticalResolution

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì.

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato dal sistema e non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=283} |             |
| 2     | /xmp/tiff:YResolution  |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                        |
|-------|-----------------------------|
| 1     | /app1/ifd/exif/{ushort=283} |
| 2     | /xmp/tiff:yresolution       |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=283}    |             |
| 2     | /ifd/xmp/tiff:YResolution |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=283}    |
| 2     | /ifd/xmp/tiff:yresolution |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Image.VerticalResolution](../properties/props-system-image-verticalresolution.md)
</dt> </dl>

 

 
