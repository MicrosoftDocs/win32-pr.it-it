---
title: Attributo WM/Year
description: L'attributo WM/Year è l'anno di pubblicazione del contenuto.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- Attributi WM/Year Windows Media Player
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec0b76fbf54a53a7ae09728fe34d75fff5c232de9ecfa13a77edaa97cd37e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900191"
---
# <a name="wmyear-attribute"></a>Attributo WM/Year

**L'attributo WM/Year** è l'anno di pubblicazione del contenuto.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi dei Windows file multimediali comunemente usati](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato solo nel file multimediale digitale.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

Questo attributo non deve essere usato come parte di una condizione di query. Deriva da un altro attributo e non può essere sottoposto direttamente a query in una raccolta di supporti.

La Windows Media Format SDK per questo attributo è g \_ wszWMYear.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 Windows Media Player 10 o versione successiva non supporta questo attributo<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





