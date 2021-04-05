---
description: Criteri di metadati della foto per la proprietà System. Photo. saturation.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Criteri dei metadati Photo System. Photo. Saturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058048"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>Criteri dei metadati Photo System. Photo. Saturation

Criteri di metadati della foto per la proprietà [System. Photo. Saturation](../properties/props-system-photo-saturation.md) .

### <a name="pkey"></a>PKEY

\_ \_ Saturazione foto pkey

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
| 1     | /App1/IFD/EXIF/{ushort = 41993} | ushort      |
| 2     | /XMP/EXIF: saturazione          | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41993} | ushort      |
| 2     | /XMP/EXIF: saturazione          | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41993} |
| 2     | /XMP/EXIF: saturazione          |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41993} | ushort      |
| 2     | /IFD/XMP/EXIF: saturazione | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41993} | ushort      |
| 2     | /IFD/XMP/EXIF: saturazione | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{ushort = 41993} |
| 2     | /IFD/XMP/EXIF: saturazione |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. saturazione](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
