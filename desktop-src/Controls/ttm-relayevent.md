---
title: TTM_RELAYEVENT messaggio (Commctrl.h)
description: Passa un messaggio del mouse a un controllo descrizione comando per l'elaborazione.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- TTM_RELAYEVENT di controllo Windows messaggio
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
ms.openlocfilehash: 051a0b7ab8ecd93b15ceb9187eefd6f566b55d653b751889cd29acec58366716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166364"
---
# <a name="ttm_relayevent-message"></a>Messaggio TTM \_ RELAYEVENT

Passa un messaggio del mouse a un controllo descrizione comando per l'elaborazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero. **Windows 7 e versioni successive:** Se la posizione della descrizione comando è offset dalla posizione del cursore (in modo da non essere ostruita da un dito o da un dispositivo di puntamento), questo parametro può contenere informazioni aggiuntive prese dal messaggio [**WM \_ MOUSEMOVE.**](/windows/desktop/inputdev/wm-mousemove) Recuperare queste informazioni aggiuntive con [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura MSG**](/windows/win32/api/winuser/ns-winuser-msg) che contiene il messaggio da inoltrare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un controllo descrizione comando elabora solo i messaggi seguenti passati dal messaggio **TTM \_ RELAYEVENT:**

-   WM \_ LBUTTONDOWN
-   WM \_ LBUTTONUP
-   WM \_ MBUTTONDOWN
-   WM \_ MBUTTONUP
-   WM \_ MOUSEMOVE
-   WM \_ NCMOUSEMOVE
-   WM \_ RBUTTONDOWN
-   WM \_ RBUTTONUP

Tutti gli altri messaggi vengono ignorati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

