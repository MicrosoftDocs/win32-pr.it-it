---
title: TDM_CLICK_RADIO_BUTTON messaggio (Commctrl.h)
description: Simula l'azione di un clic su un pulsante di opzione in una finestra di dialogo attività.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- TDM_CLICK_RADIO_BUTTON controlli Windows messaggio
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80c1eb7e72030a3c2dadc61bfd90027dab032c3342a25c72e4da9dd9a7338142
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104661"
---
# <a name="tdm_click_radio_button-message"></a>TDM \_ CLICK RADIO BUTTON \_ \_ message

Simula l'azione di un clic su un pulsante di opzione in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Valore **int** che specifica l'ID del pulsante di opzione su cui fare clic.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

L'ID del pulsante di opzione specificato viene inviato alla funzione di callback [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) come parte di un codice di notifica [TDN \_ RADIO BUTTON \_ \_ CLICKED.](tdn-radio-button-clicked.md) Al termine della funzione di callback, verrà selezionato il pulsante di opzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

