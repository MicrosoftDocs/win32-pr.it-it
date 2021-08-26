---
title: LB_GETSELITEMS messaggio (Winuser.h)
description: Riempie un buffer con una matrice di numeri interi che specificano i numeri degli elementi selezionati in una casella di riepilogo a selezione multipla.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- LB_GETSELITEMS controlli Windows messaggio
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a541c7efb0acb8d462cce42f0323393baff58e51d63e6a78a72a9d334c0eae81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085501"
---
# <a name="lb_getselitems-message"></a>Messaggio \_ LB GETSELITEMS

Riempie un buffer con una matrice di numeri interi che specificano i numeri degli elementi selezionati in una casella di riepilogo a selezione multipla.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero massimo di elementi selezionati i cui numeri di elemento devono essere inseriti nel buffer.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer sufficientemente grande per il numero di integer specificato dal *parametro wParam.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero di elementi inseriti nel buffer. Se la casella di riepilogo è una casella di riepilogo a selezione singola, il valore restituito è LB \_ ERR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ GETSELCOUNT**](lb-getselcount.md)
</dt> </dl>

 

 





