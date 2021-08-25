---
title: LB_SELITEMRANGEEX messaggio (Winuser.h)
description: Seleziona uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- LB_SELITEMRANGEEX dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e3112e36a7b212c1d0968ca738472000fabbf3d26d4d94e36ea9f21d80fe57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799441"
---
# <a name="lb_selitemrangeex-message"></a>Messaggio LB \_ SELITEMRANGEEX

Seleziona uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero del primo elemento da selezionare.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica l'indice in base zero dell'ultimo elemento da selezionare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ ERR.

## <a name="remarks"></a>Commenti

Se il *parametro wParam* è minore del *parametro lParam,* viene selezionato l'intervallo specificato di elementi. Se *wParam è* maggiore o uguale a *lParam*, l'intervallo viene rimosso dall'intervallo di elementi specificato. Per selezionare un solo elemento, selezionare due elementi e quindi deselezionare l'elemento indesiderato.

Usare questo messaggio solo con caselle di riepilogo a selezione multipla.

Questo messaggio può selezionare un intervallo solo all'interno dei primi 65.536 elementi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**LB \_ SELITEMRANGE**](lb-selitemrange.md)
</dt> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> </dl>

 

 





