---
title: Messaggio TDM_CLICK_BUTTON (COMmctrl. h)
description: Simula l'azione di un clic su un pulsante in una finestra di dialogo attività.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- Controlli di Windows Message TDM_CLICK_BUTTON
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301660"
---
# <a name="tdm_click_button-message"></a>Messaggio del pulsante di \_ clic TDM \_

Simula l'azione di un clic su un pulsante in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

**Integer** che specifica l'ID del pulsante su cui fare clic.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

L'ID del pulsante specificato da *wParam* viene inviato alla funzione di callback [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) come parte di un pulsante TDN che ha [ \_ \_ fatto clic sul](tdn-button-clicked.md) codice di notifica. Una volta restituita la funzione di callback, la finestra di dialogo attività viene chiusa se \_ dalla funzione di callback viene restituito S OK. Se \_ dalla funzione di callback viene restituito S false, la finestra di dialogo attività rimane attiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

