---
description: Criteri per i metadati delle foto per la proprietà System. image. ResolutionUnit.
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: Criteri per i metadati delle foto di System. image. ResolutionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312951"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. image. ResolutionUnit

Criteri per i metadati delle foto per la proprietà [System. image. ResolutionUnit](../properties/props-system-image-resolutionunit.md) .

### <a name="pkey"></a>PKEY

Immagine di PKEY \_ \_ ResolutionUnit

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì.

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_I2 VT

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{ushort = 296}   | ushort      |
| 2     | /xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{ushort = 296}   | ushort      |
| 2     | /xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /App1/IFD/{ushort = 296}   |
| 2     | /xmp/tiff:resolutionunit |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /IFD/{ushort = 296}            | ushort      |
| 2     | /ifd/xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /IFD/{ushort = 296}            | ushort      |
| 2     | /ifd/xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                         |
|-------|------------------------------|
| 1     | /IFD/{ushort = 296}            |
| 2     | /ifd/xmp/tiff:resolutionunit |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. image. ResolutionUnit](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
