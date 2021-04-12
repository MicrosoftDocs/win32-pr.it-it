---
description: Criteri per i metadati delle foto per la proprietà System. Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Criteri di metadati della foto di System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348596"
---
# <a name="systemcomment-photo-metadata-policy"></a>Criteri di metadati della foto di System. Comment

Criteri per i metadati delle foto per la proprietà [System. Comment](../properties/props-system-comment.md) .

### <a name="pkey"></a>PKEY

\_Commento pkey

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
| 1     | /App1/IFD/{ushort = 40092}            | \_byte Unicode |
| 2     | /App1/IFD/{ushort = 37510}            | unicode        |
| 3     | /XMP/ <xmpalt> EXIF: UserComment | unicode        |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{ushort = 40092} | \_byte Unicode |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/{ushort = 40092}      |
| 2     | /App1/IFD/EXIF/{ushort = 37510} |
| 3     | /XMP/EXIF: UserComment         |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                    | Formato disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{ushort = 40092}                     | \_byte Unicode |
| 2     | /IFD/{ushort = 37510}                     | unicode        |
| 3     | /IFD/XMP/ <xmpalt> EXIF: UserComment | unicode        |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                | Formato disco    |
|-------|---------------------|----------------|
| 1     | /IFD/{ushort = 40092} | \_byte Unicode |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /IFD/{ushort = 40092}       |
| 2     | /IFD/{ushort = 37510}       |
| 3     | /IFD/XMP/EXIF: UserComment |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
