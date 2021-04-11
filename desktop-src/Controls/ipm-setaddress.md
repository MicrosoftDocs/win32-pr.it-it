---
title: Messaggio IPM_SETADDRESS (COMmctrl. h)
description: Imposta i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- Controlli di Windows Message IPM_SETADDRESS
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120294"
---
# <a name="ipm_setaddress-message"></a>\_Messaggio di indirizzo IPM

Imposta i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore **DWORD** che contiene il nuovo indirizzo. Il valore del campo 3 è contenuto nei bit da 0 a 7. Il valore del campo 2 è contenuto in bit da 8 a 15. Il valore del campo 1 è contenuto nei bit da 16 a 23. Il valore del campo 0 è contenuto nei bit da 24 a 31. La macro [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) può essere usata anche per creare le informazioni sull'indirizzo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

Questo messaggio non genera una notifica [**IPN \_ FIELDCHANGED**](ipn-fieldchanged.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





