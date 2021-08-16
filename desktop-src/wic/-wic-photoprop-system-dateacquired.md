---
description: Criteri dei metadati della foto per la proprietà System.DateAcquired.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Criteri dei metadati delle foto System.DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95b8f68d99476db0832a321de1f61c6f3c4dc6be6f10d679735bd51fc92ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087882"
---
# <a name="systemdateacquired-photo-metadata-policy"></a>Criteri dei metadati delle foto System.DateAcquired

Criteri dei metadati della foto [per la proprietà System.DateAcquired.](../properties/props-system-dateacquired.md)

### <a name="pkey"></a>PKEY

PKEY \_ DateAcquired

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ FILETIME

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

VT \_ FILETIME

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, il gestore cerca i dati nell'ordine seguente:



| JSON | Percorso                             | Formato disco                        | Necessario |
|-------|----------------------------------|------------------------------------|----------|
| 1     | /xmp/MicrosoftPhoto:DateAcquired | Stringa Unicode in formato data XMP. | Sì      |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore cerca i dati nell'ordine seguente:



| JSON | Percorso                                 | Formato disco                        | Necessario |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:DateAcquired | Stringa Unicode in formato data XMP. | Sì      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.DateAcquired](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
