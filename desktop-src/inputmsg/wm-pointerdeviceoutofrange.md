---
title: Messaggio WM_POINTERDEVICEOUTOFRANGE
description: Inviato a una finestra quando un dispositivo puntatore ha ripartito l'intervallo di un digitalizzatore di input. Questo messaggio contiene informazioni relative al dispositivo e alla relativa prossimità.
ms.assetid: 6BC667C1-6D9A-4E69-BAC6-761A1859F09E
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERDEVICEOUTOFRANGE
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEOUTOFRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: c222d9a35cae89838d7b6e1d99dcecd11f85b54d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119495"
---
# <a name="wm_pointerdeviceoutofrange-message"></a>Messaggio WM_POINTERDEVICEOUTOFRANGE

Inviato a una finestra quando un dispositivo puntatore ha ripartito l'intervallo di un digitalizzatore di input. Questo messaggio contiene informazioni relative al dispositivo e alla relativa prossimità.

> \[! Importante\]  
> Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDEVICEOUTOFRANGE       0X23A
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

 

