---
description: Criteri per i metadati delle foto per la proprietà System. Photo. LightSource.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Criteri per i metadati delle foto di System. Photo. LightSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529935"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. LightSource

Criteri per i metadati delle foto per la proprietà [System. Photo. LightSource](../properties/props-system-photo-lightsource.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ LightSource

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
| 1     | /App1/IFD/EXIF/{ushort = 37384} | ushort      |
| 2     | /XMP/EXIF: LightSource         | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37384} | ushort      |
| 2     | /XMP/EXIF: LightSource         | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37384} |
| 2     | /XMP/EXIF: LightSource         |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37384}  | ushort      |
| 2     | /IFD/XMP/EXIF: LightSource | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37384}  | ushort      |
| 2     | /IFD/XMP/EXIF: LightSource | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{ushort = 37384}  |
| 2     | /IFD/XMP/EXIF: LightSource |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. LightSource](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
