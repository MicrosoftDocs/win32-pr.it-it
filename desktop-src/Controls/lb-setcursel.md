---
title: Messaggio LB_SETCURSEL (winuser. h)
description: Seleziona una stringa e la scorre nella visualizzazione, se necessario. Quando la nuova stringa è selezionata, la casella di riepilogo rimuove l'evidenziazione dalla stringa selezionata in precedenza.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- Controlli di Windows Message LB_SETCURSEL
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302296"
---
# <a name="lb_setcursel-message"></a>\_Messaggio con maledizione lb

Seleziona una stringa e la scorre nella visualizzazione, se necessario. Quando la nuova stringa è selezionata, la casella di riepilogo rimuove l'evidenziazione dalla stringa selezionata in precedenza.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero della stringa selezionata. Se questo parametro è-1, la casella di riepilogo è impostata su nessuna selezione.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ Err. Se il parametro *wParam* è-1, il valore restituito è lb \_ Err anche se non si è verificato alcun errore.

## <a name="remarks"></a>Commenti

Utilizzare questo messaggio solo con le caselle di riepilogo a selezione singola. Non è possibile usarlo per impostare o rimuovere una selezione in una casella di riepilogo a selezione multipla.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ GETcursel**](lb-getcursel.md)
</dt> </dl>

 

 





