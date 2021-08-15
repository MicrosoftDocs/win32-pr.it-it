---
title: WM_INPUT messaggio (Winuser.h)
description: Inviato alla finestra che sta ricevendo input non elaborato. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- WM_INPUT messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: 5d317ba21c69b22ae9c6b7cb5be0be84cd15f561b34ec65f1f99e7335cd1badb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884288"
---
# <a name="wm_input-message"></a>Messaggio \_ WM INPUT

Inviato alla finestra che sta ricevendo input non elaborato.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam*

</dt> <dd>

Codice di input. Usare la macro [**\_ \_ \_ WPARAM GET RAWINPUT CODE**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) per ottenere il valore.

I possibili valori sono i seguenti:

| Valore | Significato |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <dt>**RIM \_ INPUT**</dt> <dt>0</dt> </dl> | L'input si è verificato mentre l'applicazione era in primo piano. </br> L'applicazione deve chiamare [**DefWindowProc in**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) modo che il sistema possa eseguire la pulizia. |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <dt>**RIM \_ INPUTSINK**</dt> <dt>1</dt> </dl> | L'input si è verificato mentre l'applicazione non era in primo piano. |

</dd> <dt>

*lParam* 

</dt> <dd>

Handle **HRAWINPUT** per la [**struttura RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) che contiene l'input non elaborato dal dispositivo. Per ottenere i dati non elaborati, usare questo handle nella chiamata [**a GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

L'input non elaborato è disponibile solo quando l'applicazione chiama [**RegisterRawInputDevices con**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) specifiche di dispositivo valide.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop XP\] |
| Server minimo supportato | Windows Solo app desktop di Server 2003 \[\] |
| Intestazione | <dl> <dt>**Winuser.h (includere Windows.h)**</dt> </dl> |

## <a name="see-also"></a>Vedi anche

**Riferimento**

[**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)

[**GET \_ RAWINPUT \_ CODE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

**Informazioni concettuali**

[Input non elaborato](raw-input.md)
