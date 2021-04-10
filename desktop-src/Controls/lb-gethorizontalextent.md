---
title: Messaggio LB_GETHORIZONTALEXTENT (winuser. h)
description: Ottiene la larghezza, in pixel, in cui è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole) se nella casella di riepilogo è presente una barra di scorrimento orizzontale.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- Controlli di Windows Message LB_GETHORIZONTALEXTENT
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964858"
---
# <a name="lb_gethorizontalextent-message"></a>\_Messaggio GETHORIZONTALEXTENT lb

Ottiene la larghezza, in pixel, in cui è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole) se nella casella di riepilogo è presente una barra di scorrimento orizzontale.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la larghezza dello scorrimento, in pixel, della casella di riepilogo.

## <a name="remarks"></a>Commenti

Per rispondere al messaggio **lb \_ GETHORIZONTALEXTENT** , è necessario che la casella di riepilogo sia stata definita con lo stile [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .

Se l'applicazione non imposta l'extent orizzontale della casella di riepilogo (usando [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), l'extent orizzontale predefinito è zero. Si noti che la casella di riepilogo non aggiorna in modo dinamico l'extent orizzontale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> </dl>

 

