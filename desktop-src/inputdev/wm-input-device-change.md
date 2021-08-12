---
title: WM_INPUT_DEVICE_CHANGE messaggio (Winuser.h)
description: Inviato alla finestra registrata per ricevere input non elaborato. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- WM_INPUT_DEVICE_CHANGE messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823aeaf5655703802f07fb238d5c6c5dc479defa12ae4a416423b4519fd2b64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247887"
---
# <a name="wm_input_device_change-message"></a>WM_INPUT_DEVICE_CHANGE messaggio

## <a name="description"></a>Descrizione

Inviato alla finestra registrata per ricevere input non elaborato. 

Le notifiche di input non elaborato sono disponibili solo dopo che l'applicazione ha [chiamato RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) [con RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) flag .

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam*

</dt> <dd>

Tipo: **WPARAM**

Questo parametro può avere uno dei valori seguenti.

| Valore                    | Significato                                    |
|--------------------------|--------------------------------------------|
| **ARRIVO \_ GIDC** </br>1 | È stato aggiunto un nuovo dispositivo al sistema. </br> È possibile chiamare [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) per ottenere altre informazioni sul dispositivo. |
| **RIMOZIONE DI \_ GIDC** </br>2 | Un dispositivo è stato rimosso dal sistema. |

</dd> <dt>

*lParam* 

</dt> <dd>

Tipo: **LPARAM**

HANDLE **per** il dispositivo di input non elaborato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="see-also"></a>Vedi anche

**Informazioni concettuali**

[Input non elaborato](/windows/desktop/inputdev/raw-input)

**Riferimento**

[RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[Struttura RAWINPUTDEVICE](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

