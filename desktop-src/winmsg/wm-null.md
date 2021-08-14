---
description: Non esegue alcuna operazione. Un'applicazione invia il messaggio WM NULL se vuole pubblicare un messaggio che verrà ignorato dalla finestra \_ del destinatario.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: WM_NULL messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9ade89ee83a7d0d0b9d012248da729facbd07d269387a86cd4dfac873b76be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199947"
---
# <a name="wm_null-message"></a>Messaggio \_ NULL WM

Non esegue alcuna operazione. Un'applicazione invia **il \_ messaggio WM NULL** se vuole pubblicare un messaggio che verrà ignorato dalla finestra del destinatario.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Un'applicazione restituisce zero se elabora il messaggio.

## <a name="remarks"></a>Commenti

Ad esempio, se un'applicazione ha installato un hook **WH \_ GETMESSAGE** e vuole impedire l'elaborazione di un messaggio, la funzione di callback [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) può modificare il numero del messaggio in **WM \_ NULL** in modo che il destinatario lo ignori.

Come altro esempio, un'applicazione può controllare se una finestra risponde ai messaggi inviando il messaggio **\_ WM NULL** con la funzione [**SendMessageTimeout.**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Panoramica](windows.md)
</dt> </dl>

 

 
