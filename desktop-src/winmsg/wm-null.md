---
description: Non esegue alcuna operazione. Un'applicazione invia il \_ messaggio WM null se desidera pubblicare un messaggio che verrà ignorato dalla finestra del destinatario.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: Messaggio WM_NULL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231547"
---
# <a name="wm_null-message"></a>\_Messaggio WM null

Non esegue alcuna operazione. Un'applicazione invia il messaggio **WM \_ null** se desidera pubblicare un messaggio che verrà ignorato dalla finestra del destinatario.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NULL                         0x0000
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione restituisce zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Ad esempio, se un'applicazione ha installato un hook di **WH \_ GetMessage** e vuole impedire l'elaborazione di un messaggio, la funzione di callback [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) può modificare il numero del messaggio in **WM \_ null** , in modo che il destinatario lo ignorerà.

Un altro esempio è che un'applicazione può verificare se una finestra sta rispondendo ai messaggi inviando il messaggio **WM \_ null** con la funzione [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Windows](windows.md)
</dt> </dl>

 

 
