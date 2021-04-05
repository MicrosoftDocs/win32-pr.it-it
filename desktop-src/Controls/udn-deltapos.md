---
title: Codice di notifica UDN_DELTAPOS (COMmctrl. h)
description: Inviato dal sistema operativo alla finestra padre di un controllo di scorrimento quando la posizione del controllo sta per essere modificata.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- Controlli di Windows per il codice di notifica UDN_DELTAPOS
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
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741682"
---
# <a name="udn_deltapos-notification-code"></a>\_Codice di notifica DELTAPOS di UDN

Inviato dal sistema operativo alla finestra padre di un controllo di scorrimento quando la posizione del controllo sta per essere modificata. Questo errore si verifica quando l'utente richiede una modifica nel valore premendo la freccia su o giù del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) contenente informazioni sulla modifica della posizione. Il membro **IPO** di questa struttura contiene la posizione corrente del controllo. Il membro **oggetto IDelta** della struttura è un intero con segno che contiene la modifica proposta nella posizione. Se l'utente ha fatto clic sul pulsante verso l'alto, si tratta di un valore positivo. Se l'utente ha fatto clic sul pulsante giù, si tratta di un valore negativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per impedire la modifica nella posizione del controllo oppure zero per consentire la modifica.

## <a name="remarks"></a>Commenti

Il \_ codice di notifica DELTAPOS di UDN viene inviato prima del messaggio [**WM \_ VSCROLL**](wm-vscroll.md) o [**WM \_ HSCROLL**](wm-hscroll.md) , che modifica effettivamente la posizione del controllo. In questo modo è possibile esaminare, consentire, modificare o impedire la modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

