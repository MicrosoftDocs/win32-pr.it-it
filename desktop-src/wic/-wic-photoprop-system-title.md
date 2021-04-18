---
description: Criteri per i metadati delle foto per la proprietà System. title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Criteri per i metadati delle foto System. title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315956"
---
# <a name="systemtitle-photo-metadata-policy"></a>Criteri per i metadati delle foto System. title

Criteri per i metadati delle foto per la proprietà [System. title](../properties/props-system-title.md) .

### <a name="pkey"></a>PKEY

\_Titolo pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

VT \_ LPWSTR o VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                | Formato disco    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{ushort = 40091}            | \_byte Unicode |
| 2     | /XMP/ <xmpalt> DC: titolo         | unicode        |
| 3     | /XMP/DC: titolo                       | unicode        |
| 4     | /App1/IFD/EXIF/{ushort = 37510}       | unicode        |
| 5     | /App1/IFD/{ushort = 270}              | ascii          |
| 6     | /app13/irb/8bimiptc/iptc/caption    |                |
| 7     | /XMP/ <xmpalt> DC: Descrizione   | unicode        |
| 8     | /XMP/DC: Descrizione                 | unicode        |
| 9     | /app13/irb/8bimiptc/iptc/caption    |                |
| 10    | /XMP/ <xmpalt> EXIF: UserComment | unicode        |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                | Formato disco    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{ushort = 40091}            | \_byte Unicode |
| 2     | /XMP/DC: titolo                       | unicode        |
| 3     | /XMP/ <xmpalt> DC: titolo         | unicode        |
| 4     | /App1/IFD/EXIF/{ushort = 37510}       | unicode        |
| 5     | /XMP/ <xmpalt> EXIF: UserComment | unicode        |
| 6     | /App1/IFD/{ushort = 270}              | ascii          |
| 7     | /app13/irb/8bimiptc/iptc/caption    |                |
| 8     | /XMP/DC: Descrizione                 | unicode        |
| 9     | /XMP/ <xmpalt> DC: Descrizione   | unicode        |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                |
|-------|-------------------------------------|
| 1     | /App1/IFD/{ushort = 40091}            |
| 2     | /XMP/DC: titolo                       |
| 3     | /App1/IFD/EXIF/{ushort = 37510}       |
| 4     | /XMP/ <xmpalt> EXIF: UserComment |
| 5     | /App1/IFD/{ushort = 270}              |
| 6     | /app13/irb/8bimiptc/iptc/caption    |
| 7     | /XMP/DC: Descrizione                 |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                    | Formato disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{ushort = 40091}                     | \_byte Unicode |
| 2     | /IFD/XMP/ <xmpalt> DC: titolo         | unicode        |
| 3     | /IFD/XMP/DC: titolo                       | unicode        |
| 4     | /IFD/EXIF/{ushort = 37510}                | unicode        |
| 5     | /IFD/{ushort = 270}                       | ascii          |
| 6     | /ifd/iptc/caption                       |                |
| 7     | /IFD/XMP/ <xmpalt> DC: Descrizione   | unicode        |
| 8     | /IFD/XMP/DC: Descrizione                 | unicode        |
| 9     | /ifd/iptc/caption                       |                |
| 10    | /ifd/irb/8bimiptc/iptc/caption          |                |
| 11    | /IFD/XMP/ <xmpalt> EXIF: UserComment | unicode        |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                    | Formato disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{ushort = 40091}                     | \_byte Unicode |
| 2     | /IFD/XMP/DC: titolo                       | unicode        |
| 3     | /IFD/XMP/ <xmpalt> DC: titolo         | unicode        |
| 4     | /IFD/EXIF/{ushort = 37510}                | unicode        |
| 5     | /IFD/XMP/ <xmpalt> EXIF: UserComment | unicode        |
| 6     | /IFD/{ushort = 270}                       | ascii          |
| 7     | /ifd/iptc/caption                       |                |
| 8     | /ifd/irb/8bimiptc/iptc/caption          |                |
| 9     | /IFD/XMP/DC: Descrizione                 | unicode        |
| 10    | /IFD/XMP/ <xmpalt> DC: Descrizione   | unicode        |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                    |
|-------|-----------------------------------------|
| 1     | /IFD/{ushort = 40091}                     |
| 2     | /IFD/XMP/DC: titolo                       |
| 3     | /IFD/EXIF/{ushort = 37510}                |
| 4     | /IFD/XMP/ <xmpalt> EXIF: UserComment |
| 5     | /IFD/{ushort = 270}                       |
| 6     | /ifd/iptc/caption                       |
| 7     | /ifd/irb/8bimiptc/iptc/caption          |
| 8     | /IFD/XMP/DC: Descrizione                 |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Title](../properties/props-system-title.md)
</dt> </dl>

 

 
