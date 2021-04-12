---
title: Messaggio WM_POINTERDEVICEINRANGE
description: Inviato a una finestra quando viene rilevato un dispositivo puntatore nell'intervallo di un digitalizzatore di input. Questo messaggio contiene informazioni relative al dispositivo e alla relativa prossimità.
ms.assetid: 04244758-E662-4FB2-850E-20B4B3D1294A
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERDEVICEINRANGE
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEINRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 76ab6ac4f96d1df4e4e29afbcefe86d34b8b602d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518766"
---
# <a name="wm_pointerdeviceinrange-message"></a>Messaggio WM_POINTERDEVICEINRANGE

Inviato a una finestra quando viene rilevato un dispositivo puntatore nell'intervallo di un digitalizzatore di input. Questo messaggio contiene informazioni relative al dispositivo e alla relativa prossimità.

> \[! Importante\]  
> Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDEVICEINRANGE       0X239
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ulteriori informazioni specifiche del messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

Ulteriori informazioni specifiche del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'applicazione elabora il messaggio, deve restituire zero.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> </dl>

 

