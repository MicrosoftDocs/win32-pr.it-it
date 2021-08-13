---
title: LB_DELETESTRING messaggio (Winuser.h)
description: Elimina una stringa in una casella di riepilogo.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- LB_DELETESTRING di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329f82babea73a6392f7c360623fdeadec843dfcfd62e70106e7fb1cb0367ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671676"
---
# <a name="lb_deletestring-message"></a>Messaggio \_ LB DELETESTRING

Elimina una stringa in una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della stringa da eliminare.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un conteggio delle stringhe rimanenti nell'elenco. Il valore restituito è LB ERR se il parametro wParam specifica un indice maggiore del \_ numero di elementi nell'elenco. 

## <a name="remarks"></a>Commenti

Se un'applicazione crea la casella di riepilogo con uno stile creato dal proprietario ma senza lo stile [**\_ HASSTRINGS di LBS,**](list-box-styles.md) il sistema invia un messaggio [**WM \_ DELETEITEM**](wm-deleteitem.md) al proprietario della casella di riepilogo in modo che l'applicazione possa liberare eventuali dati aggiuntivi associati all'elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





