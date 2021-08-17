---
description: Criteri dei metadati delle foto per la proprietà System.Photo.Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Criteri dei metadati delle foto di System.Photo.Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f9496942e6be971e0e047596125669fc9112cf82bce6eb02ec7e1cdbddc4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087067"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.Photo.Orientation

Criteri dei metadati delle foto per [la proprietà System.Photo.Orientation.](../properties/props-system-photo-meteringmode.md)

### <a name="pkey"></a>Chiave PKEY

Orientamento foto \_ \_ PKEY

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

Interfaccia utente \_ VT2

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=274} | ushort      |
| 2     | /xmp/tiff:Orientation  | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=274} | ushort      |
| 2     | /xmp/tiff:Orientation  | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=274} |
| 2     | /xmp/tiff:orientation  |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort=274}         | ushort      |
| 2     | /ifd/xmp/tiff:Orientation | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort=274}         | ushort      |
| 2     | /ifd/xmp/tiff:Orientation | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /ifd/{ushort=274}         |
| 2     | /ifd/xmp/tiff:orientation |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.Orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
