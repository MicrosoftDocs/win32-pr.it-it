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
ms.openlocfilehash: 594612f3675d818f94270b1952d2a9ca7bed15d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326025"
---
# <a name="averagelevel-attribute"></a>Attributo AverageLevel

L'attributo **AverageLevel** è un valore di ampiezza a 16 bit che indica il livello medio del volume.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [File di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

Windows Media Player imposta questo valore in una delle istanze seguenti:

-   Dopo l'estrazione di un file.
-   Dopo aver riprodotto un file (quando è abilitata la funzionalità avanzata di livellamento automatico del volume).

La costante Windows Media Format SDK per questo attributo è g \_ wszAverageLevel.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





