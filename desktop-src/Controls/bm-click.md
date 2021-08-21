---
title: BM_CLICK messaggio (Winuser.h)
description: Simula l'utente che fa clic su un pulsante. Questo messaggio fa in modo che il pulsante riceva i messaggi WM LBUTTONDOWN e WM LBUTTONUP e la finestra padre del pulsante riceva un codice di notifica \_ \_ BN \_ CLICKED.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- BM_CLICK dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fdf1e206546bcdb3fa0888276414bd44b927e96a8478be4ae8a5ce2d2a5169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674983"
---
# <a name="bm_click-message"></a>Messaggio BM \_ CLICK

Simula l'utente che fa clic su un pulsante. Questo messaggio fa in modo che il pulsante riceva i messaggi [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) e [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) e la finestra padre del pulsante riceva un codice di notifica [BN \_ CLICKED.](bn-clicked.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Se il pulsante si trova in una finestra di dialogo e la finestra di dialogo non è attiva, il **messaggio BM \_ CLICK** potrebbe non riuscire. Per garantire l'esito positivo in questa situazione, chiamare la [**funzione SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) per attivare la finestra di dialogo prima di inviare il messaggio **BM \_ CLICK** al pulsante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

