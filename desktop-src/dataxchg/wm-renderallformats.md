---
title: WM_RENDERALLFORMATS messaggio (Winuser.h)
description: Inviato al proprietario degli Appunti prima dell'eliminazione, se il proprietario degli Appunti ha ritardato il rendering di uno o più formati degli Appunti.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- WM_RENDERALLFORMATS messaggio Dati Exchange
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77dae9b44cb379ed62c99c601d308fdec500440a9ebad0ffeaffad16ec780dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636061"
---
# <a name="wm_renderallformats-message"></a>Messaggio WM \_ RENDERALLFORMATS

Inviato al proprietario degli Appunti prima dell'eliminazione, se il proprietario degli Appunti ha ritardato il rendering di uno o più formati degli Appunti. Perché il contenuto degli Appunti rimanga disponibile per altre applicazioni, il proprietario degli Appunti deve eseguire il rendering dei dati in tutti i formati che è in grado di generare e inserire i dati negli Appunti chiamando la funzione [**SetClipboardData.**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Quando si risponde a un messaggio **WM \_ RENDERALLFORMATS,** l'applicazione deve chiamare la funzione [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) e quindi verificare che sia ancora il proprietario degli Appunti chiamando la [**funzione GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) prima di chiamare [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).

L'applicazione deve verificare che sia ancora il proprietario degli Appunti dopo aver aperto gli Appunti perché dopo aver ricevuto il messaggio **WM \_ RENDERALLFORMATS,** ma prima di aprire gli Appunti, un'altra applicazione potrebbe aver aperto e assunto la proprietà degli Appunti e i dati dell'applicazione non devono essere sovrascritti.

Nella maggior parte dei casi, l'applicazione non deve chiamare la funzione [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) prima di chiamare [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), poiché in questo modo verranno cancellati i formati degli Appunti di cui l'applicazione ha già eseguito il rendering.

Quando l'applicazione viene restituita, il sistema rimuove tutti i formati non di cui è stato fatto ilnder dall'elenco dei formati degli Appunti disponibili. Per informazioni sul rendering ritardato, vedere [Rendering ritardato.](clipboard-operations.md#delayed-rendering)

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

[**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM \_ RENDERFORMAT**](wm-renderformat.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 

