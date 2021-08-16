---
title: LVN_ENDSCROLL messaggio (Commctrl.h)
description: Notifica la finestra padre di un controllo visualizzazione elenco al termine di un'operazione di scorrimento. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- LVN_ENDSCROLL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d0abc3c12170dbc14f5e8a67329ed226610baa7b00fd042a24ed67193e6df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915141"
---
# <a name="lvn_endscroll-message"></a>Messaggio LVN \_ ENDSCROLL

Notifica la finestra padre di un controllo visualizzazione elenco al termine di un'operazione di scorrimento. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) che contiene la posizione orizzontale o verticale del punto in cui termina l'operazione di scorrimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore restituito non utilizzato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo codice di notifica, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





