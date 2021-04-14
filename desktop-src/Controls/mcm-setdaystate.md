---
title: Messaggio MCM_SETDAYSTATE (COMmctrl. h)
description: Imposta gli Stati del giorno per tutti i mesi attualmente visibili all'interno di un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal SetDayState.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- Controlli di Windows Message MCM_SETDAYSTATE
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478958"
---
# <a name="mcm_setdaystate-message"></a>\_Messaggio SETDAYSTATE MCM

Imposta gli Stati del giorno per tutti i mesi attualmente visibili all'interno di un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che indica il numero di elementi nella matrice a cui fa riferimento *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di valori [**MONTHDAYSTATE**](monthdaystate.md) che definiscono il modo in cui il controllo calendario mensile trarrà ogni giorno nella visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Un'applicazione può impostare in modo esplicito le informazioni sullo stato del giorno inviando questo messaggio, ma lo stato non verrà mantenuto quando una parte diversa del calendario viene visualizzata nella visualizzazione. Le informazioni sullo stato del giorno vengono in genere impostate in risposta al codice di notifica [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , che viene inviato ogni volta che è necessario aggiornare il controllo.

La matrice in *lParam* deve contenere tutti gli elementi del valore restituito dalla seguente macro:

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

Tenere presente che la matrice in *lParam* deve contenere valori [**MONTHDAYSTATE**](monthdaystate.md) che corrispondono a tutti i mesi attualmente presenti nella visualizzazione del controllo, in ordine cronologico. Sono inclusi i due mesi che possono essere visualizzati parzialmente prima del primo mese e dopo l'ultimo mese.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilizzo di controlli calendario mensile](using-month-calendar-controls.md)
</dt> </dl>

 

 





