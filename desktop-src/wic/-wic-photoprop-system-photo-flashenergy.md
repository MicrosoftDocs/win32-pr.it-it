---
description: Criteri per i metadati delle foto per la proprietà System. Photo. FlashEnergy.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: Criteri per i metadati delle foto di System. Photo. FlashEnergy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058190"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. FlashEnergy

Criteri per i metadati delle foto per la proprietà [System. Photo. FlashEnergy](../properties/props-system-photo-flashenergy.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FlashEnergy

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="input-type"></a>Tipo di input

Double

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41483} |             |
| 2     | /xmp/exif:FlashEnergy         |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41483} |             |
| 2     | /xmp/exif:FlashEnergy         |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41483} |
| 2     | /xmp/exif:flashenergy         |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41483}  |             |
| 2     | /ifd/xmp/exif:FlashEnergy |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41483}  |             |
| 2     | /ifd/xmp/exif:FlashEnergy |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{ushort = 41483}  |
| 2     | /ifd/xmp/exif:flashenergy |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. FlashEnergy](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
