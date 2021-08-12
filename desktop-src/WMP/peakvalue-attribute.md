---
title: Attributo PeakValue
description: L'attributo PeakValue è un valore di ampiezza a 16 bit che indica il livello di volume di picco.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Attributo PeakValue Windows Media Player
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a661342b305155717f4f11336f540e1ae53524ff2d303a2ab790e2c73af7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573585"
---
# <a name="peakvalue-attribute"></a>Attributo PeakValue

**L'attributo PeakValue** è un valore di ampiezza a 16 bit che indica il livello di volume di picco.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [File multimediali Windows comunemente usati](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

Windows Media Player imposta questo valore in una delle istanze seguenti:

-   Dopo aver decompresso un file.
-   Dopo aver riprodotto un file (quando è abilitato il miglioramento livellamento del volume automatico).

La Windows media format SDK costante per questo attributo è g \_ wszPeakValue.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





