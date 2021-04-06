---
description: Criteri per i metadati delle foto per la proprietà System. ApplicationName.
ms.assetid: bf4b310a-7e63-45c5-a327-2638fb31d676
title: Criteri dei metadati della foto System. ApplicationName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e36fac2a864cabfd7c1521d72357d187a8aea50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759506"
---
# <a name="systemapplicationname-photo-metadata-policy"></a>Criteri dei metadati della foto System. ApplicationName

Criteri per i metadati delle foto per la proprietà [System. ApplicationName](../properties/props-system-applicationname.md) .

### <a name="pkey"></a>PKEY

PKEY \_ ApplicationName

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

string

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                         | Formato disco |
|-------|----------------------------------------------|-------------|
|       | /App1/IFD/{ushort = 305}                       | ascii       |
|       | Programma/app13/irb/8bimiptc/iptc/Originating |             |
|       | /xmp/xmp:CreatorTool                         | unicode     |
|       | /xmp/xmp:creatortool                         | unicode     |
|       | /XMP/TIFF: software                           | unicode     |
|       | /XMP/TIFF: software                           | unicode     |
|       | Programma/app13/irb/8bimiptc/iptc/Originating |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                         | Formato disco |
|-------|----------------------------------------------|-------------|
|       | /App1/IFD/{ushort = 305}                       | ascii       |
|       | /xmp/xmp:CreatorTool                         | unicode     |
|       | /xmp/xmp:creatortool                         | unicode     |
|       | /XMP/TIFF: software                           | unicode     |
|       | /XMP/TIFF: software                           | unicode     |
|       | Programma/app13/irb/8bimiptc/iptc/Originating |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                         |
|-------|----------------------------------------------|
|       | /App1/IFD/{ushort = 305}                       |
|       | /xmp/xmp:CreatorTool                         |
|       | /xmp/xmp:creatortool                         |
|       | /XMP/TIFF: software                           |
|       | /XMP/TIFF: software                           |
|       | Programma/app13/irb/8bimiptc/iptc/Originating |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                       | Formato disco |
|-------|--------------------------------------------|-------------|
|       | /IFD/{ushort = 305}                          | ascii       |
|       | Programma/ifd/iptc/Originating              |             |
|       | /ifd/xmp/xmp:CreatorTool                   | unicode     |
|       | /ifd/xmp/xmp:creatortool                   | unicode     |
|       | /IFD/XMP/TIFF: software                     | unicode     |
|       | /IFD/XMP/TIFF: software                     | unicode     |
|       | Programma/ifd/iptc/Originating              |             |
|       | Programma/ifd/irb/8bimiptc/iptc/Originating |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                       | Formato disco |
|-------|--------------------------------------------|-------------|
|       | /IFD/{ushort = 305}                          | ascii       |
|       | /ifd/xmp/xmp:CreatorTool                   | unicode     |
|       | /ifd/xmp/xmp:creatortool                   | unicode     |
|       | /IFD/XMP/TIFF: software                     | unicode     |
|       | /IFD/XMP/TIFF: software                     | unicode     |
|       | Programma/ifd/iptc/Originating              |             |
|       | Programma/ifd/irb/8bimiptc/iptc/Originating |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                       |
|-------|--------------------------------------------|
|       | /IFD/{ushort = 305}                          |
|       | /ifd/xmp/xmp:CreatorTool                   |
|       | /ifd/xmp/xmp:creatortool                   |
|       | /IFD/XMP/TIFF: software                     |
|       | /IFD/XMP/TIFF: software                     |
|       | Programma/ifd/iptc/Originating              |
|       | Programma/ifd/irb/8bimiptc/iptc/Originating |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. ApplicationName](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
