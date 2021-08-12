---
title: Attributo AverageLevel
description: L'attributo AverageLevel è un valore di ampiezza a 16 bit che indica il livello medio del volume.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- Attributo AverageLevel Windows Media Player
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e169b1e2d63e6f8215515acc852d431ff13ccd513924e4c2a237b16c17dacfc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582746"
---
# <a name="averagelevel-attribute"></a>Attributo AverageLevel

**L'attributo AverageLevel** è un valore di ampiezza a 16 bit che indica il livello medio del volume.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [File multimediali Windows comunemente usati](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

Windows Media Player imposta questo valore in una delle istanze seguenti:

-   Dopo aver decompresso un file.
-   Dopo aver riprodotto un file (quando è abilitato il miglioramento livellamento del volume automatico).

La Windows media format SDK costante per questo attributo è g \_ wszAverageLevel.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





