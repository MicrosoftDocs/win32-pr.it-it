---
title: Messaggio WM_INPUT_DEVICE_CHANGE (winuser. h)
description: Inviato alla finestra registrata per ricevere input non elaborato. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- Input della tastiera e del mouse WM_INPUT_DEVICE_CHANGE messaggio
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
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "104047537"
---
# <a name="wm_input_device_change-message"></a>Messaggio WM_INPUT_DEVICE_CHANGE

## <a name="description"></a>Descrizione

Inviato alla finestra registrata per ricevere input non elaborato. 

Le notifiche di input non elaborate sono disponibili solo dopo che l'applicazione chiama [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) con [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) flag.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam*

</dt> <dd>

Tipo: **wParam**

Questo parametro può avere uno dei valori seguenti.

| Valore                    | Significato                                    |
|--------------------------|--------------------------------------------|
| **GIDC \_ arrivo** </br>1 | Al sistema è stato aggiunto un nuovo dispositivo. </br> È possibile chiamare [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) per ottenere altre informazioni sul dispositivo. |
| **rimozione di GIDC \_** </br>2 | Un dispositivo è stato rimosso dal sistema. |

</dd> <dt>

*lParam* 

</dt> <dd>

Tipo: **lParam**

**Handle** per il dispositivo di input non elaborato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="see-also"></a>Vedi anche

**Informazioni concettuali**

[Input non elaborato](/windows/desktop/inputdev/raw-input)

**Riferimento**

[RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[Struttura RAWINPUTDEVICE](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

