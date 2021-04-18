---
title: Messaggio WM_POINTERDEVICECHANGE
description: Inviato a una finestra quando viene apportata una modifica alle impostazioni di un monitoraggio a cui è collegato un digitalizzatore. Questo messaggio contiene informazioni sul ridimensionamento della modalità di visualizzazione.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERDEVICECHANGE
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
ms.openlocfilehash: 38f570059f374f64e393e960a8458e605983d6c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302073"
---
# <a name="wm_pointerdevicechange-message"></a>Messaggio WM_POINTERDEVICECHANGE

Inviato a una finestra quando viene apportata una modifica alle impostazioni di un monitoraggio a cui è collegato un digitalizzatore. Questo messaggio contiene informazioni sul ridimensionamento della modalità di visualizzazione.

> \[! Importante\]  
> Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene un valore delle [**costanti di modifica del dispositivo puntatore**](pointer-device-change-constants.md).

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

 

