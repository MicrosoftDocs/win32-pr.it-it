---
description: Criteri per i metadati delle foto per la proprietà System. GPS. ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Criteri per i metadati delle foto di System. GPS. ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233535"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. ImgDirectionRef

Criteri per i metadati delle foto per la proprietà [System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS. ImgDirectionRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policies"></a>Criteri di JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{ushort = 16}    |
| 2     | /xmp/exif:gpsimgdirectionref |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{ushort = 16}             |
| 2     | /ifd/xmp/exif:gpsimgdirectionref |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
