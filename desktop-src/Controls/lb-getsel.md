---
title: LB_GETSEL messaggio (Winuser.h)
description: Ottiene lo stato di selezione di un elemento.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- LB_GETSEL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e27a1bcec021d7416e32d1bae4047f7b2705e347cc396a07dcf6c377ccb48f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085511"
---
# <a name="lb_getsel-message"></a>Messaggio \_ LB GETSEL

Ottiene lo stato di selezione di un elemento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero di un elemento.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se viene selezionato un elemento, il valore restituito è maggiore di zero. in caso contrario, è zero. Se si verifica un errore, il valore restituito è LB \_ ERR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> </dl>

 

 





