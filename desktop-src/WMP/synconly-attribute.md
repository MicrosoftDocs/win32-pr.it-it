---
title: Attributo SyncOnly
description: L'attributo SyncOnly è una rappresentazione di stringa di un valore booleano Windows Media Player per determinare se una playlist è disponibile solo per la sincronizzazione.
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
ms.openlocfilehash: e77fe67fe3cb943ad210f4d9beb58cfea8f32da87e6ee15955b578f07a608f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134734"
---
# <a name="synconly-attribute"></a>Attributo SyncOnly

**L'attributo SyncOnly** è una  rappresentazione di stringa di un valore booleano Windows Media Player per determinare se una playlist è disponibile solo per la sincronizzazione.

## <a name="applies-to"></a>Si applica a

-   [Playlist](playlist-attributes-ref.md)

## <a name="remarks"></a>Commenti

Il valore 1 indica che la playlist è disponibile solo per la sincronizzazione e non può essere visualizzata nel **nodo Playlist** automatica. Il valore zero indica che la playlist può essere visualizzata nel **nodo Playlist** automatica.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





