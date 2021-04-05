---
title: Messaggio LB_SETHORIZONTALEXTENT (winuser. h)
description: Imposta la larghezza, in pixel, in base alla quale è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- Controlli di Windows Message LB_SETHORIZONTALEXTENT
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874338"
---
# <a name="lb_sethorizontalextent-message"></a>\_Messaggio SETHORIZONTALEXTENT lb

Imposta la larghezza, in pixel, in base alla quale è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole). Se la larghezza della casella di riepilogo è inferiore a questo valore, la barra di scorrimento orizzontale scorre orizzontalmente gli elementi nella casella di riepilogo. Se la larghezza della casella di riepilogo è maggiore o uguale a questo valore, la barra di scorrimento orizzontale viene nascosta.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il numero di pixel in base al quale è possibile scorrere la casella di riepilogo.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Per rispondere al messaggio **lb \_ SETHORIZONTALEXTENT** , è necessario che la casella di riepilogo sia stata definita con lo stile [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .

Si noti che una casella di riepilogo non aggiorna in modo dinamico l'extent orizzontale.

Questo messaggio non ha alcun effetto su una casella di riepilogo a più colonne.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETHORIZONTALEXTENT lb**](lb-gethorizontalextent.md)
</dt> </dl>

 

