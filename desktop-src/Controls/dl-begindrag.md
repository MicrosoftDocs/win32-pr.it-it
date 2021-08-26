---
title: DL_BEGINDRAG di notifica (Commctrl.h)
description: Notifica alla finestra padre della casella di riepilogo di trascinamento che l'utente ha fatto clic con il pulsante sinistro del mouse su un elemento. Una casella di riepilogo di trascinamento invia questo codice di notifica sotto forma di messaggio di elenco di trascinamento. Per altre informazioni, vedere Trascinare i messaggi della casella di riepilogo.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- DL_BEGINDRAG del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2c843398b21ad51df51ae706a515c2e6f9831b89d32092b87148598b4bed5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968331"
---
# <a name="dl_begindrag-notification-code"></a>Codice di notifica DL \_ BEGINDRAG

Notifica alla finestra padre della casella di riepilogo di trascinamento che l'utente ha fatto clic con il pulsante sinistro del mouse su un elemento. Una casella di riepilogo di trascinamento invia questo codice di notifica sotto forma di messaggio di elenco di trascinamento. Per altre informazioni, vedere [Trascinare messaggi della casella di riepilogo.](about-list-boxes.md)


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) che contiene il codice di notifica DL BEGINDRAG, l'handle per la casella di riepilogo di trascinamento \_ e la posizione del cursore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire **TRUE per** avviare l'operazione di trascinamento oppure FALSE **per** impedire l'operazione di trascinamento.

## <a name="remarks"></a>Commenti

Quando si elabora questo codice di notifica, una routine della finestra determina in genere l'elemento dell'elenco in corrispondenza della posizione del cursore specificata usando [**la funzione LBItemFromPt.**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) Restituisce quindi **TRUE** o **FALSE,** a seconda che l'elemento debba essere trascinato. Prima di restituire **TRUE,** la routine della finestra deve salvare l'indice dell'elemento dell'elenco in modo che l'applicazione sappia quale elemento spostare o copiare al termine dell'operazione di trascinamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





