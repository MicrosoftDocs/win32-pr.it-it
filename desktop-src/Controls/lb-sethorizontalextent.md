---
title: LB_SETHORIZONTALEXTENT messaggio (Winuser.h)
description: Imposta la larghezza, in pixel, in base alla quale una casella di riepilogo può essere scorrevole orizzontalmente (larghezza scorrevole).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- LB_SETHORIZONTALEXTENT di controllo Windows messaggio
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
ms.openlocfilehash: ce248354b853dd3be15e76646958ed25068648182970d748da35fb5c596ca49e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433880"
---
# <a name="lb_sethorizontalextent-message"></a>Messaggio \_ LB SETHORIZONTALEXTENT

Imposta la larghezza, in pixel, in base alla quale una casella di riepilogo può essere scorrevole orizzontalmente (larghezza scorrevole). Se la larghezza della casella di riepilogo è inferiore a questo valore, la barra di scorrimento orizzontale scorre orizzontalmente gli elementi nella casella di riepilogo. Se la larghezza della casella di riepilogo è uguale o maggiore di questo valore, la barra di scorrimento orizzontale è nascosta.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il numero di pixel in base al quale è possibile scorrere la casella di riepilogo.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Per rispondere al **messaggio LB \_ SETHORIZONTALEXTENT,** la casella di riepilogo deve essere stata definita con lo [**stile \_ HSCROLL WS.**](/windows/desktop/winmsg/window-styles)

Si noti che una casella di riepilogo non aggiorna dinamicamente l'extent orizzontale.

Questo messaggio non ha effetto su una casella di riepilogo a più colonne.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md)
</dt> </dl>

 

