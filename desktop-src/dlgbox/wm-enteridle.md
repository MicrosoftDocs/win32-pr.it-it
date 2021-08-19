---
title: WM_ENTERIDLE messaggio (Winuser.h)
description: Inviato alla finestra proprietaria di una finestra di dialogo modale o di un menu che entra in uno stato di inattività. Una finestra di dialogo modale o un menu entra in uno stato di inattività quando nessun messaggio è in attesa nella coda dopo aver elaborato uno o più messaggi precedenti.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- WM_ENTERIDLE finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb7d40ae84659d1cfad12357956c4a955ae4f879cddcc13b51069a6a62cd08c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985281"
---
# <a name="wm_enteridle-message"></a>Messaggio \_ WM ENTERIDLE

Inviato alla finestra proprietaria di una finestra di dialogo modale o di un menu che entra in uno stato di inattività. Una finestra di dialogo modale o un menu entra in uno stato di inattività quando nessun messaggio è in attesa nella coda dopo aver elaborato uno o più messaggi precedenti.


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                   | Significato                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <dt>**MSGF \_ DIALOGBOX**</dt> <dt>0</dt> </dl> | Il sistema è inattivo perché viene visualizzata una finestra di dialogo.<br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <dt>**MSGF \_ MENU**</dt> <dt>2</dt> </dl>                | Il sistema è inattivo perché viene visualizzato un menu.<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la finestra di dialogo *(se wParam* è **MSGF \_ DIALOGBOX**) o finestra contenente il menu visualizzato (se *wParam* è **MSGF \_ MENU**).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

È possibile eliminare il **messaggio WM \_ ENTERIDLE** per una finestra di dialogo creando la finestra di dialogo con lo stile **\_ DS NOIDLEMSG.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> </dl>

 

