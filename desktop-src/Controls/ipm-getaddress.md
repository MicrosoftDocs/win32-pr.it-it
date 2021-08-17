---
title: IPM_GETADDRESS messaggio (Commctrl.h)
description: Ottiene i valori degli indirizzi per tutti e quattro i campi nel controllo indirizzo IP.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- IPM_GETADDRESS controlli di Windows messaggio
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bcb35ed71532e815b33b45e1c15e9b82b75b5c87fac406b52de80670e3d72a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434513"
---
# <a name="ipm_getaddress-message"></a>Messaggio \_ IPM GETADDRESS

Ottiene i valori degli indirizzi per tutti e quattro i campi nel controllo indirizzo IP.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un **valore DWORD** che riceve l'indirizzo. Il valore del campo 3 sarà contenuto nei bit da 0 a 7. Il valore del campo 2 sarà contenuto nei bit da 8 a 15. Il valore del campo 1 sarà contenuto nei bit da 16 a 23. Il valore del campo 0 sarà contenuto nei bit da 24 a 31. Le macro [**FIRST \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), [**SECOND \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**THIRD \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)e [**FOURTH \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) possono essere usate anche per estrarre le informazioni sull'indirizzo. Come indirizzo per tutti i campi vuoti verrà restituito zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di campi non blank.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





