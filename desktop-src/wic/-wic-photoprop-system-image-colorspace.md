---
description: Criteri per i metadati delle foto per la proprietà System. image. TextSpazio.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Criteri per i metadati delle foto System. image. TextSpazio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312957"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a>Criteri per i metadati delle foto System. image. TextSpazio

Criteri per i metadati delle foto per la proprietà [System. image. TextSpazio](../properties/props-system-image-colorspace.md) .

### <a name="pkey"></a>PKEY

\_ \_ Spazio colore immagine pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_UI2 VT

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /XMP/EXIF: spazio colore          | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /XMP/EXIF: spazio colore          | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 40961} |
| 2     | /XMP/EXIF: spazio colore          |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /IFD/XMP/EXIF: spazio colore | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /IFD/XMP/EXIF: spazio colore | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{ushort = 40961} |
| 2     | /IFD/XMP/EXIF: spazio colore |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. image. spazio colore](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
