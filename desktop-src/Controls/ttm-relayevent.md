---
title: Messaggio TTM_RELAYEVENT (COMmctrl. h)
description: Passa un messaggio del mouse a un controllo ToolTip per l'elaborazione.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- Controlli di Windows Message TTM_RELAYEVENT
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353251"
---
# <a name="ttm_relayevent-message"></a>\_Messaggio TTM RELAYEVENT

Passa un messaggio del mouse a un controllo ToolTip per l'elaborazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero. **Windows 7 e versioni successive:** Se la posizione della descrizione comando viene sfalsata rispetto alla posizione del cursore (in modo che non venga ostacolata da un dito o da un dispositivo di puntamento), questo parametro può contenere informazioni aggiuntive tratte dal messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . Recuperare queste informazioni aggiuntive con [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) che contiene il messaggio da inoltrare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un controllo ToolTip elabora solo i messaggi seguenti passati dal messaggio **TTM \_ RELAYEVENT** :

-   \_LBUTTONDOWN WM
-   \_LBUTTONUP WM
-   \_MBUTTONDOWN WM
-   \_MBUTTONUP WM
-   MOUSEMOVE di WM \_
-   \_NCMOUSEMOVE WM
-   \_RBUTTONDOWN WM
-   \_RBUTTONUP WM

Tutti gli altri messaggi vengono ignorati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

