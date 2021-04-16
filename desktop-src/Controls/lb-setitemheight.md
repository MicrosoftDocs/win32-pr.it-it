---
title: Messaggio LB_SETITEMHEIGHT (winuser. h)
description: Imposta l'altezza, in pixel, degli elementi in una casella di riepilogo. Se la casella di riepilogo ha lo \_ stile OwnerDrawVariable lbs, questo messaggio imposta l'altezza dell'elemento specificato dal parametro wParam. In caso contrario, in questo messaggio viene impostata l'altezza di tutti gli elementi nella casella di riepilogo.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- Controlli di Windows Message LB_SETITEMHEIGHT
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
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478539"
---
# <a name="lb_setitemheight-message"></a>\_Messaggio SETITEMHEIGHT lb

Imposta l'altezza, in pixel, degli elementi in una casella di riepilogo. Se la casella di riepilogo ha lo stile [**\_ OwnerDrawVariable lbs**](list-box-styles.md) , questo messaggio imposta l'altezza dell'elemento specificato dal parametro *wParam* . In caso contrario, in questo messaggio viene impostata l'altezza di tutti gli elementi nella casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero dell'elemento nella casella di riepilogo. Usare questo parametro solo se la casella di riepilogo ha lo stile [**\_ OwnerDrawVariable lbs**](list-box-styles.md) . in caso contrario, impostarla su zero.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica l'altezza, in pixel, dell'elemento. L'altezza massima è 255 pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'indice o l'altezza non è valido, il valore restituito è LB \_ Err.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETITEMHEIGHT lb**](lb-getitemheight.md)
</dt> </dl>

 

 





