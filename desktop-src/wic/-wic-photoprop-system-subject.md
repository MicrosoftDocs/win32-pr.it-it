---
description: Criteri per i metadati delle foto per la proprietà System. Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Criteri per i metadati della foto System. Subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315957"
---
# <a name="systemsubject-photo-metadata-policy"></a>Criteri per i metadati della foto System. Subject

Criteri per i metadati delle foto per la proprietà [System. Subject](../properties/props-system-subject.md) .

### <a name="pkey"></a>PKEY

\_Oggetto pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

VT \_ LPWSTR o VT \_ LPWSTR

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{ushort = 40095} | \_byte Unicode |
| 2     | /App1/IFD/{ushort = 270}   | ascii          |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{ushort = 40095} | \_byte Unicode |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /App1/IFD/{ushort = 40095} |
| 2     | /App1/IFD/{ushort = 270}   |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                | Formato disco    |
|-------|---------------------|----------------|
| 1     | /IFD/{ushort = 40095} | \_byte Unicode |
| 2     | /IFD/{ushort = 270}   | ascii          |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                | Formato disco    |
|-------|---------------------|----------------|
| 1     | /IFD/{ushort = 40095} | \_byte Unicode |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                |
|-------|---------------------|
| 1     | /IFD/{ushort = 40095} |
| 2     | /IFD/{ushort = 270}   |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Subject](../properties/props-system-subject.md)
</dt> </dl>

 

 
