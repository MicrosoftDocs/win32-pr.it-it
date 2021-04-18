---
description: Criteri per i metadati delle foto per la proprietà System. Photo. PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Criteri per i metadati delle foto di System. Photo. PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3de9f5adda67fcd0e555194500f109df078bdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315966"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. PeopleNames

Criteri per i metadati delle foto per la proprietà [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ PeopleNames

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ vettore \| VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

StringMulti

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                                           | Formato disco |
|-------|----------------------------------------------------------------|-------------|
| 1     | /XMP/ <xmpstruct> MP: RegionInfo/ <xmpbag> MPRI: aree | ushort      |



 

### <a name="write-paths"></a>Percorsi di scrittura

Questa proprietà non può essere scritta usando i criteri dei metadati.

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                |
|-------|-------------------------------------|
| 1     | <xmpstruct>MP/XMP/: RegionInfo |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                                               | Formato disco |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /IFD/XMP/ <xmpstruct> MP: RegionInfo/ <xmpbag> MPRI: aree | ushort      |



 

### <a name="write-paths"></a>Percorsi di scrittura

Questa proprietà non può essere scritta usando i criteri dei metadati.

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                    |
|-------|-----------------------------------------|
| 1     | <xmpstruct>MP/IFD/XMP/: RegionInfo |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
