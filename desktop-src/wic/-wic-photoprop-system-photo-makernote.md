---
description: Criteri per i metadati delle foto per la proprietà System. Photo. MakerNote.
ms.assetid: e1018bc6-3fd2-4212-afee-6811bfe99f14
title: Criteri per i metadati delle foto di System. Photo. MakerNote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df1a16205d6a9d1229d3627e6b9cc8c746d8a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312943"
---
# <a name="systemphotomakernote-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. MakerNote

Criteri per i metadati delle foto per la proprietà [System. Photo. Makernote](../properties/props-system-photo-makernote.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ Makernote

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_VTUI1 vettore \| VT

### <a name="input-type"></a>Tipo di input

Buffer

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37500} |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37500} |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37500} |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37500} |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37500} |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{ushort = 37500} |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. MakerNote](../properties/props-system-photo-makernote.md)
</dt> </dl>

 

 
