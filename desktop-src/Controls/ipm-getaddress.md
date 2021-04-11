---
title: Messaggio IPM_GETADDRESS (COMmctrl. h)
description: Ottiene i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- Controlli di Windows Message IPM_GETADDRESS
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
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964476"
---
# <a name="ipm_getaddress-message"></a>\_Messaggio IPM GETaddress

Ottiene i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un valore **DWORD** che riceve l'indirizzo. Il valore del campo 3 sarà contenuto nei bit da 0 a 7. Il valore del campo 2 sarà contenuto in bit da 8 a 15. Il valore del campo 1 sarà contenuto nei bit da 16 a 23. Il valore del campo 0 sarà contenuto nei bit da 24 a 31. Per estrarre le informazioni sull'indirizzo, è inoltre possibile utilizzare le [**prime \_**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)macro IPAddress, [**Second \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**Third \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)e [**Fourth \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) . Zero verrà restituito come indirizzo per tutti i campi vuoti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di campi non vuoti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





