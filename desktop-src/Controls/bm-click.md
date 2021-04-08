---
title: Messaggio BM_CLICK (winuser. h)
description: Simula l'utente che fa clic su un pulsante. Questo messaggio fa in modo che il pulsante riceva i \_ messaggi WM LBUTTONDOWN e WM \_ LBUTTONUP e la finestra padre del pulsante per ricevere un \_ codice di notifica fatto clic su BN.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- Controlli di Windows Message BM_CLICK
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
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048070"
---
# <a name="bm_click-message"></a>\_Messaggio di clic BM

Simula l'utente che fa clic su un pulsante. Questo messaggio fa in modo che il pulsante riceva i messaggi [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) e [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) e la finestra padre del pulsante per ricevere un codice di notifica [ \_ fatto clic su BN](bn-clicked.md) .

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

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Se il pulsante si trova in una finestra di dialogo e la finestra di dialogo non è attiva, il messaggio di **\_ clic BM** potrebbe non riuscire. Per garantire l'esito positivo della situazione, chiamare la funzione [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) per attivare la finestra di dialogo prima di inviare il messaggio di **\_ clic BM** al pulsante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



 

