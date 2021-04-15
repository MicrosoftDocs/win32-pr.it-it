---
title: Messaggio RB_BEGINDRAG (COMmctrl. h)
description: Inserisce il controllo Rebar in modalità di trascinamento della selezione. Questo messaggio non comporta l' \_ invio di una notifica RBN BEGINDRAG.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- Controlli di Windows Message RB_BEGINDRAG
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477890"
---
# <a name="rb_begindrag-message"></a>\_Messaggio BEGINDRAG RB

Inserisce il controllo Rebar in modalità di trascinamento della selezione. Questo messaggio non comporta l'invio di una notifica [RBN \_ BEGINDRAG](rbn-begindrag.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda che avrà effetto sull'operazione di trascinamento della selezione.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore **DWORD** che contiene le coordinate iniziali del mouse. La coordinata orizzontale è contenuta in LOWORD e la coordinata verticale è contenuta in HIWORD. Se si passa (**DWORD**)-1, il controllo Rebar utilizzerà la posizione del mouse nell'ultima volta in cui il thread del controllo ha chiamato [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="remarks"></a>Commenti

I **messaggi \_ RB BEGINDRAG**, [**RB \_ DRAGMOVE**](rb-dragmove.md)e [**RB \_ ENDDRAG**](rb-enddrag.md) consentono di implementare un'interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) per un controllo Rebar. Inviare il messaggio **RB \_ BEGINDRAG** in risposta a [**IDropTarget::D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), inviare il messaggio **RB \_ DRAGMOVE** in risposta a [**IDropTarget::D Ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)e il messaggio **RB \_ ENDDRAG** in risposta a [**IDropTarget::D por**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) e [**IDropTarget::D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

