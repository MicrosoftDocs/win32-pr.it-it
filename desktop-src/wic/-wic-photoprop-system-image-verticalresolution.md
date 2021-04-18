---
description: Criteri per i metadati delle foto per la proprietà System. image. VerticalResolution.
ms.assetid: a58b7463-3572-4ca8-8299-93d92d2f06fb
title: Criteri per i metadati delle foto di System. image. VerticalResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e895ef9e1181a3ec40b474940c6dfaaa3e1329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312944"
---
# <a name="systemimageverticalresolution-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. image. VerticalResolution

Criteri per i metadati delle foto per la proprietà [System. image. VerticalResolution](../properties/props-system-image-verticalresolution.md) .

### <a name="pkey"></a>PKEY

Immagine di PKEY \_ \_ VerticalResolution

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì.

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato dal sistema e non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 283} |             |
| 2     | /XMP/TIFF: YResolution  |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                        |
|-------|-----------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 283} |
| 2     | /XMP/TIFF: YResolution       |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 283}    |             |
| 2     | /IFD/XMP/TIFF: YResolution |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{ushort = 283}    |
| 2     | /IFD/XMP/TIFF: YResolution |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. image. VerticalResolution](../properties/props-system-image-verticalresolution.md)
</dt> </dl>

 

 
