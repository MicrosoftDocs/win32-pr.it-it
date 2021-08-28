---
title: UDN_DELTAPOS di notifica (Commctrl.h)
description: Inviato dal sistema operativo alla finestra padre di un controllo di tipo up-down quando la posizione del controllo sta per cambiare.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81285d2e0aa5c9a8b65eabf7c5b23d02da3acf02ac13e3274accce340530024f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088411"
---
# <a name="udn_deltapos-notification-code"></a>Codice di notifica DELTAPOS UDN \_

Inviato dal sistema operativo alla finestra padre di un controllo di tipo up-down quando la posizione del controllo sta per cambiare. Ciò si verifica quando l'utente richiede una modifica al valore premendo la freccia su o giù del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) che contiene informazioni sulla modifica della posizione. Il **membro iPos** di questa struttura contiene la posizione corrente del controllo. Il **membro iDelta** della struttura è un intero con segno che contiene la modifica proposta nella posizione. Se l'utente ha fatto clic sul pulsante su, si tratta di un valore positivo. Se l'utente ha fatto clic sul pulsante verso il basso, si tratta di un valore negativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per impedire la modifica della posizione del controllo oppure zero per consentire la modifica.

## <a name="remarks"></a>Commenti

Il codice di notifica DELTAPOS UDN viene inviato prima del messaggio \_ [**WM \_ VSCROLL**](wm-vscroll.md) o [**WM \_ HSCROLL,**](wm-hscroll.md) che modifica effettivamente la posizione del controllo. In questo modo è possibile esaminare, consentire, modificare o non consentire la modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

