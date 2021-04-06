---
description: Criteri per i metadati delle foto per la proprietà System. Photo. TranscodedForSync.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Criteri per i metadati delle foto di System. Photo. TranscodedForSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883970"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. TranscodedForSync

Criteri per i metadati delle foto per la proprietà [System. Photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ TranscodedForSync

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_bool VT

### <a name="input-type"></a>Tipo di input

Proprietà di tipo Boolean.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                  | Formato disco  |
|-------|---------------------------------------|--------------|
| 1     | /App1/IFD/{ushort = 18248}              | ushort di bool \_ |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                  | Formato disco  |
|-------|---------------------------------------|--------------|
| 1     | /App1/IFD/{ushort = 18248}              | ushort di bool \_ |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                  |
|-------|---------------------------------------|
| 1     | /App1/IFD/{ushort = 18248}              |
| 2     | /xmp/microsoftphoto:transcodedforsync |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                      | Formato disco  |
|-------|-------------------------------------------|--------------|
| 1     | /IFD/{ushort = 18248}                       | ushort di bool \_ |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                      | Formato disco  |
|-------|-------------------------------------------|--------------|
| 1     | /IFD/{ushort = 18248}                       | ushort di bool \_ |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                      |
|-------|-------------------------------------------|
| 1     | /IFD/{ushort = 18248}                       |
| 2     | /ifd/xmp/microsoftphoto:transcodedforsync |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
