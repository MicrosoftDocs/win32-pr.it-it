---
description: Criteri per i metadati delle foto per la proprietà System. Photo. FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Criteri per i metadati delle foto di System. Photo. FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c518ef2a05dde8fd7e812d1d76a79cbe3efb4217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232314"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. FNumber

Criteri per i metadati delle foto per la proprietà [System. Photo. fnumber](../properties/props-system-photo-fnumber.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ fnumber

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. Photo. FNumberNumerator e System. Photo. FNumberDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 33437} |             |
| 2     | /xmp/exif:FNumber             |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



|       |                               |             |     |
|-------|-------------------------------|-------------|-----|
| JSON | Percorso                          | Formato disco |     |
| 1     | /App1/IFD/EXIF/{ushort = 33437} |             |     |
| 2     | /xmp/exif:FNumber             |             |     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 33437} |
| 2     | /xmp/exif:fnumber             |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 33437} |             |
| 2     | /ifd/xmp/exif:FNumber    |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 33437} |             |
| 2     | /ifd/xmp/exif:FNumber    |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{ushort = 33437} |
| 2     | /ifd/xmp/exif:fnumber    |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. FNumber](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
