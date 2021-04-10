---
title: Messaggio TDM_CLICK_RADIO_BUTTON (COMmctrl. h)
description: Simula l'azione di un pulsante di opzione fare clic in una finestra di dialogo attività.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- Controlli di Windows Message TDM_CLICK_RADIO_BUTTON
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
ms.openlocfilehash: b76d465b1b937359a3d312a401914d497f9c9b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964851"
---
# <a name="tdm_click_radio_button-message"></a>TDM \_ fare clic sul \_ pulsante di opzione \_

Simula l'azione di un pulsante di opzione fare clic in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Valore **int** che specifica l'ID del pulsante di opzione su cui fare clic.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

L'ID del pulsante di opzione specificato viene inviato alla funzione di callback [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) come parte di un [pulsante di \_ opzione TDN \_ \_ selezionato](tdn-radio-button-clicked.md) . Dopo che la funzione di callback viene restituita, il pulsante di opzione verrà selezionato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

