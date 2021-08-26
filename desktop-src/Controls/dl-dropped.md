---
title: DL_DROPPED di notifica (Commctrl.h)
description: Segnala che l'utente ha completato un'operazione di trascinamento rilasciando il pulsante sinistro del mouse. Una casella di riepilogo di trascinamento invia questo codice di notifica alla relativa finestra padre sotto forma di messaggio di elenco di trascinamento. Per altre informazioni, vedere Trascinare i messaggi della casella di riepilogo.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c245cbb85a4e67845bd86a25b4cccb2f2aa0dc1d9d9613afd1d685037c5e1ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002721"
---
# <a name="dl_dropped-notification-code"></a>Codice di notifica DL \_ DROPPED

Segnala che l'utente ha completato un'operazione di trascinamento rilasciando il pulsante sinistro del mouse. Una casella di riepilogo di trascinamento invia questo codice di notifica alla relativa finestra padre sotto forma di messaggio di elenco di trascinamento. Per altre informazioni, vedere [Trascinare i messaggi della casella di riepilogo.](about-list-boxes.md)


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) che contiene il codice di notifica DL DROPPED, l'handle per la casella di riepilogo di trascinamento \_ e la posizione del cursore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene in genere elaborato inserendo l'elemento trascinato nell'elenco davanti all'elemento sotto il cursore. Per recuperare l'indice dell'elemento in corrispondenza della posizione del cursore, usare la [**funzione LBItemFromPt.**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) Si noti che il codice di notifica DL \_ DROPPED viene inviato anche se il cursore non si trova su un elemento dell'elenco. In tal caso, **LBItemFromPt** restituisce -1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





