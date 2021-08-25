---
title: LB_SETCURSEL messaggio (Winuser.h)
description: Seleziona una stringa e la scorre nella visualizzazione, se necessario. Quando si seleziona la nuova stringa, la casella di riepilogo rimuove l'evidenziazione dalla stringa selezionata in precedenza.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- LB_SETCURSEL di controllo Windows messaggio
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
ms.openlocfilehash: b33964d98717ab84a325b5070eec6c4e1cacf334ba2272d4691d340a15af78a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085341"
---
# <a name="lb_setcursel-message"></a>Messaggio \_ LB SETCURSEL

Seleziona una stringa e la scorre nella visualizzazione, se necessario. Quando si seleziona la nuova stringa, la casella di riepilogo rimuove l'evidenziazione dalla stringa selezionata in precedenza.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero della stringa selezionata. Se questo parametro è -1, la casella di riepilogo viene impostata in modo che non abbia alcuna selezione.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ ERR. Se il *parametro wParam* è -1, il valore restituito è LB \_ ERR anche se non si è verificato alcun errore.

## <a name="remarks"></a>Commenti

Usare questo messaggio solo con caselle di riepilogo a selezione singola. Non è possibile usarlo per impostare o rimuovere una selezione in una casella di riepilogo a selezione multipla.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ GETCURSEL**](lb-getcursel.md)
</dt> </dl>

 

 





