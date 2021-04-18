---
description: Criteri per i metadati delle foto per la proprietà System. Photo. WhiteBalance.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: Criteri per i metadati delle foto di System. Photo. WhiteBalance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315958"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. WhiteBalance

Criteri per i metadati delle foto per la proprietà [System. Photo. whitebalance](../properties/props-system-photo-whitebalance.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ whitebalance

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
| 1     | /App1/IFD/EXIF/{ushort = 41987} | ushort      |
| 2     | /XMP/EXIF: WhiteBalance        | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41987} | ushort      |
| 2     | /XMP/EXIF: WhiteBalance        | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41987} |
| 2     | /XMP/EXIF: whitebalance        |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41987}   | ushort      |
| 2     | /IFD/XMP/EXIF: WhiteBalance | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41987}   | ushort      |
| 2     | /IFD/XMP/EXIF: WhiteBalance | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{ushort = 41987}   |
| 2     | /IFD/XMP/EXIF: whitebalance |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. WhiteBalance](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
