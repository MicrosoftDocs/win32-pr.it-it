---
title: LB_SETTOPINDEX messaggio (Winuser.h)
description: Assicura che l'elemento specificato in una casella di riepilogo sia visibile.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_settopindex.htm
keywords:
- LB_SETTOPINDEX di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b640b55ed2c6e3e38eea0b8bd23eb4f99d770dd49b4499f054f5ec38b71873
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435461"
---
# <a name="lb_settopindex-message"></a>Messaggio \_ LB SETTOPINDEX

Assicura che l'elemento specificato in una casella di riepilogo sia visibile.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento nella casella di riepilogo.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ ERR.

## <a name="remarks"></a>Commenti

Il sistema scorre il contenuto della casella di riepilogo in modo che l'elemento specificato venga visualizzato nella parte superiore della casella di riepilogo o che sia stato raggiunto l'intervallo di scorrimento massimo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ GETTOPINDEX**](lb-gettopindex.md)
</dt> </dl>

 

 





