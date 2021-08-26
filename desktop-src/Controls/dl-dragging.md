---
title: DL_DRAGGING codice di notifica (Commctrl.h)
description: Segnala che l'utente ha spostato il mouse durante il trascinamento di un elemento.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- DL_DRAGGING codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe07cbf2cce3ad639af94055a2d1eab1f4fc3d6ce576c1c5467310809858843
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878521"
---
# <a name="dl_dragging-notification-code"></a>Codice di notifica DL \_ DRAGGING

Segnala che l'utente ha spostato il mouse durante il trascinamento di un elemento. DL DRAGGING viene inviato periodicamente anche \_ durante il trascinamento anche se il mouse non viene spostato. Una casella di riepilogo di trascinamento invia questo codice di notifica alla relativa finestra padre sotto forma di messaggio dell'elenco di trascinamento. Per altre informazioni, vedere [Trascinare i messaggi della casella di riepilogo.](about-list-boxes.md)


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di controllo della casella di riepilogo di trascinamento.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) che contiene il codice di notifica DL DRAGGING, l'handle per la casella di riepilogo di trascinamento \_ e la posizione del cursore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito determina il tipo di cursore del mouse che deve essere impostato dall'elenco di trascinamento. può essere il valore DL \_ STOPCURSOR, DL \_ COPYCURSOR o DL \_ MOVECURSOR. Se viene restituito qualsiasi altro valore, il cursore non cambia.

## <a name="remarks"></a>Commenti

Una routine della finestra elabora in genere il codice di notifica DL DRAGGING determinando l'elemento sotto il cursore e disegnando \_ un'icona di inserimento. Per recuperare l'elemento sotto il cursore, usare la [**funzione LBItemFromPt,**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) specificando **TRUE** per il *parametro bAutoScroll.* Questa opzione fa scorrere periodicamente la casella di riepilogo di trascinamento se il cursore si trova sopra o sotto la relativa area client. Per disegnare l'icona di inserimento, usare la [**funzione DrawInsert.**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





