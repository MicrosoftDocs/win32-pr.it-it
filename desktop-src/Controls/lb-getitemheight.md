---
title: Messaggio LB_GETITEMHEIGHT (winuser. h)
description: Ottiene l'altezza degli elementi in una casella di riepilogo.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- Controlli di Windows Message LB_GETITEMHEIGHT
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873661"
---
# <a name="lb_getitemheight-message"></a>\_Messaggio GETITEMHEIGHT lb

Ottiene l'altezza degli elementi in una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento della casella di riepilogo. Questo indice viene usato solo se la casella di riepilogo ha lo stile [**\_ OwnerDrawVariable lbs**](list-box-styles.md) . in caso contrario, deve essere zero.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'altezza, in pixel, di ogni elemento nella casella di riepilogo. Il valore restituito è l'altezza dell'elemento specificato dal parametro *wParam* se la casella di riepilogo ha lo stile [**\_ OwnerDrawVariable lbs**](list-box-styles.md) . Il valore restituito è LB \_ Err se si verifica un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETITEMHEIGHT lb**](lb-setitemheight.md)
</dt> </dl>

 

 





