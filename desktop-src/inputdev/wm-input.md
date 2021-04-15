---
title: Messaggio WM_INPUT (winuser. h)
description: Inviato alla finestra che sta ricevendo l'input non elaborato. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- Input della tastiera e del mouse WM_INPUT messaggio
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
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400505"
---
# <a name="wm_input-message"></a>\_Messaggio di input WM

Inviato alla finestra che sta ricevendo l'input non elaborato.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam*

</dt> <dd>

Codice di input. Per ottenere il valore, usare [**get \_ rawinput \_ Code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) macro.

I possibili valori sono i seguenti:

| Valore | Significato |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <dt>**Cerchio \_ INPUT**</dt> <dt>0</dt> </dl> | L'input si è verificato mentre l'applicazione era in primo piano. </br> L'applicazione deve chiamare [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) in modo che il sistema possa eseguire la pulizia. |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <dt>**Cerchio \_ INPUTSINK**</dt> <dt>1</dt> </dl> | Si è verificato un input mentre l'applicazione non è in primo piano. |

</dd> <dt>

*lParam* 

</dt> <dd>

Handle **HRAWINPUT** per la struttura [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) che contiene l'input non elaborato dal dispositivo. Per ottenere i dati non elaborati, usare questo handle nella chiamata a [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

L'input non elaborato è disponibile solo quando l'applicazione chiama [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) con specifiche del dispositivo valide.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | \[Solo app desktop Windows XP\] |
| Server minimo supportato | \[Solo app desktop Windows Server 2003\] |
| Intestazione | <dl> <dt>**Winuser. h (include Windows. h)**</dt> </dl> |

## <a name="see-also"></a>Vedi anche

**Riferimento**

[**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)

[**OTTENERE \_ il \_ codice rawinput \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

**Informazioni concettuali**

[Input non elaborato](raw-input.md)
