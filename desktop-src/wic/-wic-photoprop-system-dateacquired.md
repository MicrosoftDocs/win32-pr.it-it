---
description: Criteri per i metadati delle foto per la proprietà System. DateAcquired.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Criteri per i metadati delle foto System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233538"
---
# <a name="systemdateacquired-photo-metadata-policy"></a>Criteri per i metadati delle foto System. DateAcquired

Criteri per i metadati delle foto per la proprietà [System. DateAcquired](../properties/props-system-dateacquired.md) .

### <a name="pkey"></a>PKEY

\_DATEACQUIRED pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

FILETIME VT \_

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

FILETIME VT \_

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, il gestore cerca i dati nell'ordine seguente:



| JSON | Percorso                             | Formato disco                        | Necessario |
|-------|----------------------------------|------------------------------------|----------|
| 1     | /xmp/MicrosoftPhoto:DateAcquired | Stringa Unicode nel formato di data XMP. | Sì      |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore cerca i dati nell'ordine seguente:



| JSON | Percorso                                 | Formato disco                        | Necessario |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:DateAcquired | Stringa Unicode nel formato di data XMP. | Sì      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. DateAcquired](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
