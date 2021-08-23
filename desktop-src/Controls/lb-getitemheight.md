---
title: LB_GETITEMHEIGHT messaggio (Winuser.h)
description: Ottiene l'altezza degli elementi in una casella di riepilogo.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- LB_GETITEMHEIGHT di controllo Windows messaggio
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
ms.openlocfilehash: 29c232c172f14774db9dd7c783e18a10f0888190708432b9336208570f0d5031
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434331"
---
# <a name="lb_getitemheight-message"></a>Messaggio \_ LB GETITEMHEIGHT

Ottiene l'altezza degli elementi in una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento della casella di riepilogo. Questo indice viene utilizzato solo se la casella di riepilogo ha lo stile [**LBS \_ OWNERDRAWVARIABLE;**](list-box-styles.md) in caso contrario, deve essere zero.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'altezza, in pixel, di ogni elemento nella casella di riepilogo. Il valore restituito è l'altezza dell'elemento specificato dal *parametro wParam* se la casella di riepilogo ha lo stile [**LBS \_ OWNERDRAWVARIABLE.**](list-box-styles.md) Il valore restituito è LB \_ ERR se si verifica un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ SETITEMHEIGHT**](lb-setitemheight.md)
</dt> </dl>

 

 





