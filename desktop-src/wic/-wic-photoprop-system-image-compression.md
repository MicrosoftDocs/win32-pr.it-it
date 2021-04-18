---
description: Criteri di metadati della foto per la proprietà System. image. Compression.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: Criteri dei metadati della foto di System. image. Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312954"
---
# <a name="systemimagecompression-photo-metadata-policy"></a>Criteri dei metadati della foto di System. image. Compression

Criteri di metadati della foto per la proprietà [System. image. Compression](../properties/props-system-image-compression.md) .

### <a name="pkey"></a>PKEY

\_Compressione immagini \_ pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_UI2 VT

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 259} | ushort      |
| 2     | /XMP/TIFF: compressione  | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 259} | ushort      |
| 2     | /XMP/TIFF: compressione  | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                   |
|-------|------------------------|
| 1     | /App1/IFD/{ushort = 259} |
| 2     | /XMP/TIFF: compressione  |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 259}         | ushort      |
| 2     | /IFD/XMP/TIFF: compressione | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 259}         | ushort      |
| 2     | /IFD/XMP/TIFF: compressione | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /IFD/{ushort = 259}         |
| 2     | /IFD/XMP/TIFF: compressione |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. image. Compression](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
