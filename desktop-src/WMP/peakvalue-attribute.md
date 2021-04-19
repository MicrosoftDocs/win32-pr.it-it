---
title: Attributo PeakValue
description: L'attributo PeakValue è un valore di ampiezza a 16 bit che indica il livello di picco del volume.
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
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332678"
---
# <a name="peakvalue-attribute"></a>Attributo PeakValue

L'attributo **PeakValue** è un valore di ampiezza a 16 bit che indica il livello di picco del volume.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [File di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

Windows Media Player imposta questo valore in una delle istanze seguenti:

-   Dopo l'estrazione di un file.
-   Dopo aver riprodotto un file (quando è abilitata la funzionalità avanzata di livellamento automatico del volume).

La costante Windows Media Format SDK per questo attributo è g \_ wszPeakValue.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





