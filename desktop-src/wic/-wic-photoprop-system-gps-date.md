---
description: Criteri per i metadati delle foto per la proprietà System. GPS. date.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: Criteri dei metadati della foto System. GPS. date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233537"
---
# <a name="systemgpsdate-photo-metadata-policy"></a>Criteri dei metadati della foto System. GPS. date

Criteri per i metadati delle foto per la proprietà [System. GPS. date](../properties/props-system-gps-date.md) .

### <a name="pkey"></a>PKEY

\_Data GPS \_ pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policies"></a>Criteri di JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 29} |
| 2     | /xmp/exif:GPSTimeStamp    |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{ushort = 29}       |
| 2     | /ifd/xmp/exif:GPSTimeStamp |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. date](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
