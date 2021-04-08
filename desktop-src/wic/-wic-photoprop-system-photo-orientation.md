---
description: Criteri di metadati della foto per la proprietà System. Photo. Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Criteri dei metadati delle foto di System. Photo. Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058049"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a>Criteri dei metadati delle foto di System. Photo. Orientation

Criteri di metadati della foto per la proprietà [System. Photo. Orientation](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>PKEY

\_Orientamento foto \_ pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

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
| 1     | /App1/IFD/{ushort = 274} | ushort      |
| 2     | /XMP/TIFF: orientamento  | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 274} | ushort      |
| 2     | /XMP/TIFF: orientamento  | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                   |
|-------|------------------------|
| 1     | /App1/IFD/{ushort = 274} |
| 2     | /XMP/TIFF: orientamento  |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF: orientamento | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF: orientamento | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /IFD/{ushort = 274}         |
| 2     | /IFD/XMP/TIFF: orientamento |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. Orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
