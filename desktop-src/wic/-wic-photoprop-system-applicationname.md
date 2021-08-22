---
description: Criteri dei metadati delle foto per la proprietà System.ApplicationName.
ms.assetid: bf4b310a-7e63-45c5-a327-2638fb31d676
title: Criteri metadati foto System.ApplicationName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3084f21453a82c79925d4a164f5f847c3a24968009b7b8c4236ce3a40872dad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710920"
---
# <a name="systemapplicationname-photo-metadata-policy"></a>Criteri metadati foto System.ApplicationName

Criteri dei metadati delle foto per [la proprietà System.ApplicationName.](../properties/props-system-applicationname.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ ApplicationName

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

string

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                         | Formato disco |
|-------|----------------------------------------------|-------------|
|       | /app1/ifd/{ushort=305}                       | ascii       |
|       | /app13/irb/8bimiptc/iptc/Originating Program |             |
|       | /xmp/xmp:CreatorTool                         | unicode     |
|       | /xmp/xmp:creatortool                         | unicode     |
|       | /xmp/tiff:Software                           | unicode     |
|       | /xmp/tiff:software                           | unicode     |
|       | /app13/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                         | Formato disco |
|-------|----------------------------------------------|-------------|
|       | /app1/ifd/{ushort=305}                       | ascii       |
|       | /xmp/xmp:CreatorTool                         | unicode     |
|       | /xmp/xmp:creatortool                         | unicode     |
|       | /xmp/tiff:Software                           | unicode     |
|       | /xmp/tiff:software                           | unicode     |
|       | /app13/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                         |
|-------|----------------------------------------------|
|       | /app1/ifd/{ushort=305}                       |
|       | /xmp/xmp:CreatorTool                         |
|       | /xmp/xmp:creatortool                         |
|       | /xmp/tiff:Software                           |
|       | /xmp/tiff:software                           |
|       | /app13/irb/8bimiptc/iptc/Originating Program |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                       | Formato disco |
|-------|--------------------------------------------|-------------|
|       | /ifd/{ushort=305}                          | ascii       |
|       | /ifd/iptc/Originating Program              |             |
|       | /ifd/xmp/xmp:CreatorTool                   | unicode     |
|       | /ifd/xmp/xmp:creatortool                   | unicode     |
|       | /ifd/xmp/tiff:Software                     | unicode     |
|       | /ifd/xmp/tiff:software                     | unicode     |
|       | /ifd/iptc/Originating Program              |             |
|       | /ifd/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                       | Formato disco |
|-------|--------------------------------------------|-------------|
|       | /ifd/{ushort=305}                          | ascii       |
|       | /ifd/xmp/xmp:CreatorTool                   | unicode     |
|       | /ifd/xmp/xmp:creatortool                   | unicode     |
|       | /ifd/xmp/tiff:Software                     | unicode     |
|       | /ifd/xmp/tiff:software                     | unicode     |
|       | /ifd/iptc/Originating Program              |             |
|       | /ifd/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                       |
|-------|--------------------------------------------|
|       | /ifd/{ushort=305}                          |
|       | /ifd/xmp/xmp:CreatorTool                   |
|       | /ifd/xmp/xmp:creatortool                   |
|       | /ifd/xmp/tiff:Software                     |
|       | /ifd/xmp/tiff:software                     |
|       | /ifd/iptc/Originating Program              |
|       | /ifd/irb/8bimiptc/iptc/Originating Program |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.ApplicationName](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
