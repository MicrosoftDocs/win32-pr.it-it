---
description: Inviato quando l'utente elimina un file nella finestra di un'applicazione che si è registrata come destinatario dei file eliminati.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: WM_DROPFILES messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c36043997b4d462b5d453952f690cc8569218c398796b6a42b10709053b0d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118046482"
---
# <a name="wm_dropfiles-message"></a>Messaggio \_ WM DROPFILES

Inviato quando l'utente elimina un file nella finestra di un'applicazione che si è registrata come destinatario dei file eliminati.


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

Handle a una struttura interna che descrive i file eliminati. Passare questo handle [**DragFinish,**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish) [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)o [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) per recuperare informazioni sui file rilasciati.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

L'handle HDROP è dichiarato in Shellapi.h. È necessario includere questa intestazione nella compilazione per usare **WM \_ DROPFILES.** Per altre informazioni su come usare il trascinamento della selezione per trasferire i dati della shell, vedere [Transferring Shell Data Using Drag-and-Drop or the Clipboard](dragdrop.md)(Trasferimento di dati della shell tramite trascinamento della selezione o Appunti).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**DragAcceptFiles**](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
