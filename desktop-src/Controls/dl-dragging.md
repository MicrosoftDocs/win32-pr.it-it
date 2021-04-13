---
title: Codice di notifica DL_DRAGGING (COMmctrl. h)
description: Segnala che l'utente ha spostato il mouse durante il trascinamento di un elemento.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- Controlli di Windows per il codice di notifica DL_DRAGGING
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
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519334"
---
# <a name="dl_dragging-notification-code"></a>Codice di notifica per il \_ trascinamento DL

Segnala che l'utente ha spostato il mouse durante il trascinamento di un elemento. \_Anche il trascinamento DL DL viene inviato periodicamente durante il trascinamento anche se il mouse non viene spostato. Una casella di riepilogo di trascinamento Invia questo codice di notifica alla finestra padre sotto forma di messaggio elenco di trascinamento. Per ulteriori informazioni, vedere [trascinare i messaggi della casella di riepilogo](about-list-boxes.md).


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

Puntatore a una struttura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) che contiene il \_ codice di notifica di trascinamento DL, l'handle per la casella di riepilogo di trascinamento e la posizione del cursore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito determina il tipo di cursore del mouse che deve essere impostato dall'elenco di trascinamento. può essere il valore DL \_ STOPCURSOR, DL \_ COPYCURSOR o DL \_ MOVECURSOR. Se viene restituito qualsiasi altro valore, il cursore non viene modificato.

## <a name="remarks"></a>Commenti

Una routine della finestra elabora in genere il \_ codice di notifica di trascinamento del DL, determinando l'elemento sotto il cursore e quindi disegnando un'icona di inserimento. Per recuperare l'elemento sotto il cursore, utilizzare la funzione [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) , specificando **true** per il parametro *bAutoScroll* . Questa opzione fa in modo che la casella di riepilogo di trascinamento scorra periodicamente se il cursore si trova sopra o sotto la relativa area client. Per creare l'icona Inserisci, utilizzare la funzione [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





