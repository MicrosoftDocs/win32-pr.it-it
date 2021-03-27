---
description: Inviato quando l'utente rilascia un file nella finestra di un'applicazione che si è registrato come destinatario di file eliminati.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: Messaggio WM_DROPFILES (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979466"
---
# <a name="wm_dropfiles-message"></a>\_Messaggio DropFiles WM

Inviato quando l'utente rilascia un file nella finestra di un'applicazione che si è registrato come destinatario di file eliminati.


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDrop* 
</dt> <dd>

Handle per una struttura interna che descrive i file eliminati. Passare questo handle [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)o [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) per recuperare le informazioni sui file eliminati.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

L'handle HDROP è dichiarato in Shellapi. h. Per usare **WM \_ DropFiles**, è necessario includere questa intestazione nella compilazione. Per altre informazioni su come usare il trascinamento della selezione per trasferire i dati della shell, vedere [trasferimento di dati della shell tramite il trascinamento della selezione o gli appunti](dragdrop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**DragAcceptFiles**](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
