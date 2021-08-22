---
title: LB_SETITEMHEIGHT messaggio (Winuser.h)
description: Imposta l'altezza, in pixel, degli elementi in una casella di riepilogo. Se la casella di riepilogo ha lo stile LBS OWNERDRAWVARIABLE, questo messaggio imposta l'altezza \_ dell'elemento specificato dal parametro wParam. In caso contrario, questo messaggio imposta l'altezza di tutti gli elementi nella casella di riepilogo.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- LB_SETITEMHEIGHT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd661c9fb32d2cbe0763f8c138d133f8a32b46d17201b33033b832aeb8cb49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433871"
---
# <a name="lb_setitemheight-message"></a>Messaggio \_ LB SETITEMHEIGHT

Imposta l'altezza, in pixel, degli elementi in una casella di riepilogo. Se la casella di riepilogo ha lo stile [**LBS \_ OWNERDRAWVARIABLE,**](list-box-styles.md) questo messaggio imposta l'altezza dell'elemento specificato dal *parametro wParam.* In caso contrario, questo messaggio imposta l'altezza di tutti gli elementi nella casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero dell'elemento nella casella di riepilogo. Utilizzare questo parametro solo se la casella di riepilogo ha lo stile [**LBS \_ OWNERDRAWVARIABLE;**](list-box-styles.md) in caso contrario, impostarlo su zero.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica l'altezza, in pixel, dell'elemento. L'altezza massima è di 255 pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'indice o l'altezza non è valido, il valore restituito è LB \_ ERR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)
</dt> </dl>

 

 





