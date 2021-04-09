---
title: Messaggio LB_GETSELITEMS (winuser. h)
description: Riempie un buffer con una matrice di Integer che specificano i numeri degli elementi selezionati in una casella di riepilogo a selezione multipla.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- Controlli di Windows Message LB_GETSELITEMS
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
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964294"
---
# <a name="lb_getselitems-message"></a>\_Messaggio GETSELITEMS lb

Riempie un buffer con una matrice di Integer che specificano i numeri degli elementi selezionati in una casella di riepilogo a selezione multipla.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero massimo di elementi selezionati i cui numeri di elemento devono essere inseriti nel buffer.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer sufficientemente grande per il numero di numeri interi specificati dal parametro *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero di elementi inseriti nel buffer. Se la casella di riepilogo è una casella di riepilogo a selezione singola, il valore restituito è LB \_ Err.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETSELCOUNT lb**](lb-getselcount.md)
</dt> </dl>

 

 





