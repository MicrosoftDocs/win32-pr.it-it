---
description: Criteri di metadati della foto per la proprietà System. Photo. Contrast.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Criteri dei metadati della foto System. Photo. Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530264"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a>Criteri dei metadati della foto System. Photo. Contrast

Criteri di metadati della foto per la proprietà [System. Photo. Contrast](../properties/props-system-photo-contrast.md) .

### <a name="pkey"></a>PKEY

\_Contrasto foto \_ pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_UI4 VT

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /XMP/EXIF: contrasto            | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /XMP/EXIF: contrasto            | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41992} |
| 2     | /XMP/EXIF: contrasto            |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /IFD/XMP/EXIF: contrasto   | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41992} | ushort      |
| 2     | /IFD/XMP/EXIF: contrasto   | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{ushort = 41992} |
| 2     | /IFD/XMP/EXIF: contrasto   |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. Contrast](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
