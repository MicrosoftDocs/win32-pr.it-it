---
description: Criteri per i metadati delle foto per la proprietà System. Photo. Nitidity.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Criteri dei metadati della foto System. Photo. nitidezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315964"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a>Criteri dei metadati della foto System. Photo. nitidezza

Criteri per i metadati delle foto per la proprietà [System. Photo. nitidity](../properties/props-system-photo-sharpness.md) .

### <a name="pkey"></a>PKEY

\_ \_ Nitidezza foto pkey

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
| 1     | /App1/IFD/EXIF/{ushort = 41994} | ushort      |
| 2     | /XMP/EXIF: nitidezza           | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41994} | ushort      |
| 2     | /XMP/EXIF: nitidezza           | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41994} |
| 2     | /XMP/EXIF: nitidezza           |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41994} | ushort      |
| 2     | /IFD/XMP/EXIF: nitidezza  | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41994} | ushort      |
| 2     | /IFD/XMP/EXIF: nitidezza  | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{ushort = 41994} |
| 2     | /IFD/XMP/EXIF: nitidezza  |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. nitidezza](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
