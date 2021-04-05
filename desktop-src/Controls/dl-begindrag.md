---
title: Codice di notifica DL_BEGINDRAG (COMmctrl. h)
description: Notifica alla finestra padre della casella di riepilogo di trascinamento che l'utente ha fatto clic con il pulsante sinistro del mouse su un elemento. Una casella di riepilogo di trascinamento Invia questo codice di notifica sotto forma di messaggio elenco di trascinamento. Per ulteriori informazioni, vedere trascinare i messaggi della casella di riepilogo.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- Controlli di Windows per il codice di notifica DL_BEGINDRAG
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
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874722"
---
# <a name="dl_begindrag-notification-code"></a>\_Codice di notifica BEGINDRAG DL

Notifica alla finestra padre della casella di riepilogo di trascinamento che l'utente ha fatto clic con il pulsante sinistro del mouse su un elemento. Una casella di riepilogo di trascinamento Invia questo codice di notifica sotto forma di messaggio elenco di trascinamento. Per ulteriori informazioni, vedere [trascinare i messaggi della casella di riepilogo](about-list-boxes.md).


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) che contiene il \_ codice di notifica BEGINDRAG DL, l'handle per la casella di riepilogo di trascinamento e la posizione del cursore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per avviare l'operazione di trascinamento oppure **false** per impedire l'operazione di trascinamento.

## <a name="remarks"></a>Commenti

Quando si elabora questo codice di notifica, una routine della finestra determina in genere l'elemento dell'elenco in corrispondenza della posizione del cursore specificata tramite la funzione [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) . Restituisce quindi **true** o **false**, a seconda che l'elemento debba essere trascinato. Prima di restituire **true**, la routine della finestra deve salvare l'indice dell'elemento di elenco in modo che l'applicazione conosca quale elemento spostare o copiare al termine dell'operazione di trascinamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





