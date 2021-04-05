---
title: Criteri per i metadati delle foto di System. image. HorizontalResolution
description: Criteri per i metadati delle foto per la proprietà System. image. HorizontalResolution.
ms.assetid: 1fe73c50-4179-4ea4-be1c-9e103fb65d59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade406e644524fea84ef6baf957aed661d2adf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756917"
---
# <a name="systemimagehorizontalresolution-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. image. HorizontalResolution

Criteri per i metadati delle foto per la proprietà [System. image. HorizontalResolution](../properties/props-system-image-horizontalresolution.md) .

### <a name="pkey"></a>PKEY

Immagine di PKEY \_ \_ HorizontalResolution

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
| 1     | /App1/IFD/{ushort = 282} |             |
| 2     | /XMP/TIFF: XResolution  |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                        | Formato del disco |
|-------|-----------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 282} |             |
| 2     | /XMP/TIFF: XResolution       |             |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 282}    |             |
| 2     | /IFD/XMP/TIFF: XResolution |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      | Formato del disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 282}    |             |
| 2     | /IFD/XMP/TIFF: XResolution |             |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. image. HorizontalResolution](../properties/props-system-image-horizontalresolution.md)
</dt> </dl>

 

 
