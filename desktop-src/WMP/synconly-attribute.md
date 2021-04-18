---
title: Attributo SyncOnly
description: L'attributo SyncOnly è una rappresentazione di stringa di un valore booleano usato da Windows Media Player per determinare se una playlist è disponibile solo per la sincronizzazione.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Attributo SyncOnly Windows Media Player
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325579"
---
# <a name="synconly-attribute"></a>Attributo SyncOnly

L'attributo **SyncOnly** è una rappresentazione di stringa di un valore **booleano** usato da Windows Media Player per determinare se una playlist è disponibile solo per la sincronizzazione.

## <a name="applies-to"></a>Si applica a

-   [Playlist](playlist-attributes-ref.md)

## <a name="remarks"></a>Commenti

Il valore 1 indica che la playlist è disponibile solo per la sincronizzazione e non può essere visualizzata nel nodo **playlist automatico** . Un valore pari a zero indica che la playlist può essere visualizzata nel nodo **playlist automatico** .

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





