---
title: Codice di notifica DL_DROPPED (COMmctrl. h)
description: Segnala che l'utente ha completato un'operazione di trascinamento rilasciando il pulsante sinistro del mouse. Una casella di riepilogo di trascinamento Invia questo codice di notifica alla finestra padre sotto forma di messaggio elenco di trascinamento. Per ulteriori informazioni, vedere trascinare i messaggi della casella di riepilogo.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- Controlli di Windows per il codice di notifica DL_DROPPED
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
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874725"
---
# <a name="dl_dropped-notification-code"></a>\_Codice di notifica eliminato DL

Segnala che l'utente ha completato un'operazione di trascinamento rilasciando il pulsante sinistro del mouse. Una casella di riepilogo di trascinamento Invia questo codice di notifica alla finestra padre sotto forma di messaggio elenco di trascinamento. Per ulteriori informazioni, vedere [trascinare i messaggi della casella di riepilogo](about-list-boxes.md).


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) che contiene il \_ codice di notifica rilasciato DL, l'handle per la casella di riepilogo di trascinamento e la posizione del cursore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene in genere elaborato inserendo l'elemento trascinato nell'elenco davanti all'elemento sotto il cursore. Per recuperare l'indice dell'elemento in corrispondenza della posizione del cursore, utilizzare la funzione [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) . Si noti che il \_ codice di notifica eliminato DL viene inviato anche se il cursore non si trova in un elemento elenco. In tal caso, **LBItemFromPt** restituisce-1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





