---
description: Criteri dei metadati della foto per la proprietà System.Photo.FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Criteri metadati foto System.Photo.FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85443b849d9f810709f3e75c3082738e5377092f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443622"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a>Criteri metadati foto System.Photo.FNumber

Criteri dei metadati della foto per [la proprietà System.Photo.FNumber.](../properties/props-system-photo-fnumber.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FNumber

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System.Photo.FNumberNumerator e System.Photo.FNumberDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| Ordine | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=33437} |             |
| 2     | /xmp/exif:FNumber             |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| Ordine | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=33437} |             |
| 2     | /xmp/exif:FNumber             |             | 
 

### <a name="remove-paths"></a>Rimuovere i percorsi



| Ordine | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=33437} |
| 2     | /xmp/exif:fnumber             |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| Ordine | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=33437} |             |
| 2     | /ifd/xmp/exif:FNumber    |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| Ordine | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=33437} |             |
| 2     | /ifd/xmp/exif:FNumber    |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| Ordine | Percorso                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=33437} |
| 2     | /ifd/xmp/exif:fnumber    |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.FNumber](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
