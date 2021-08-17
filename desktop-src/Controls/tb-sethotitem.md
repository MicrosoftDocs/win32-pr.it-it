---
title: TB_SETHOTITEM messaggio (Commctrl.h)
description: "TB_SETHOTITEM: imposta l'elemento di scelta rapida in una barra degli strumenti."
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM controlli di Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a48de58e07d877d999c2d0388bf32845fce349511da563c3a6b1fa9f9c7b3d20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318841"
---
# <a name="tb_sethotitem-message"></a>TB \_ SETHOTITEM message

Imposta l'elemento a caldo in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento che verrà reso ad caldo. Se questo valore è -1, nessuno degli elementi sarà ad accesso hot.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento corrente precedente oppure -1 se non è presente alcun elemento di tipo hot.

## <a name="remarks"></a>Commenti

Il comportamento di questo messaggio non è definito per le barre degli strumenti che non hanno lo stile [**FLAT TBSTYLE. \_**](toolbar-control-and-button-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





