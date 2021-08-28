---
title: WM_POINTERDEVICECHANGE messaggio
description: Inviato a una finestra quando viene apportata una modifica alle impostazioni di un monitor a cui è collegato un digitalizzatore. Questo messaggio contiene informazioni relative al ridimensionamento della modalità di visualizzazione.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- WM_POINTERDEVICECHANGE messaggi di input e notifiche del messaggio
topic_type:
- apiref
api_name:
- WM_POINTERDEVICECHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6d75a5afa245303952c5c6b1814b2f1ce77cd03da7c789d34bda2500c6bffee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829581"
---
# <a name="wm_pointerdevicechange-message"></a>WM_POINTERDEVICECHANGE messaggio

Inviato a una finestra quando viene apportata una modifica alle impostazioni di un monitor a cui è collegato un digitalizzatore. Questo messaggio contiene informazioni relative al ridimensionamento della modalità di visualizzazione.

> \[! Importante\]  
> Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi dell'indicatore di misura e nelle strutture correlate potrebbero apparire inaccurate a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto per il ridimensionamento automatico per le applicazioni che non sono in grado di riconoscere DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene un valore da [**Pointer Device Change Constants**](pointer-device-change-constants.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Ulteriori informazioni specifiche del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'applicazione elabora questo messaggio, deve restituire zero.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                               |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> </dl>

 

