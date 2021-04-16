---
title: Messaggio WM_RENDERALLFORMATS (winuser. h)
description: Inviato al proprietario degli Appunti prima che venga eliminato definitivamente, se il proprietario degli Appunti ha ritardato il rendering di uno o più formati degli Appunti.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- Scambio di dati del messaggio WM_RENDERALLFORMATS
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
ms.openlocfilehash: 6cdd3ce1fabdea4cdcae93b5243b89c53def0afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518555"
---
# <a name="wm_renderallformats-message"></a>\_Messaggio RENDERALLFORMATS WM

Inviato al proprietario degli Appunti prima che venga eliminato definitivamente, se il proprietario degli Appunti ha ritardato il rendering di uno o più formati degli Appunti. Affinché il contenuto degli Appunti rimanga disponibile per altre applicazioni, il proprietario degli Appunti deve eseguire il rendering dei dati in tutti i formati che è in grado di generare e inserire i dati negli Appunti chiamando la funzione [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Quando si risponde a un messaggio **WM \_ RENDERALLFORMATS** , l'applicazione deve chiamare la funzione [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) e quindi verificare che sia ancora il proprietario degli Appunti chiamando la funzione [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) prima di chiamare [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).

L'applicazione deve verificare che sia il proprietario degli Appunti dopo aver aperto gli appunti, perché dopo aver ricevuto il messaggio **WM \_ RENDERALLFORMATS** , ma prima di aprire gli appunti, è possibile che un'altra applicazione abbia aperto e assunto la proprietà degli Appunti e che i dati dell'applicazione non vengano sovrascritti.

Nella maggior parte dei casi, l'applicazione non deve chiamare la funzione [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) prima di chiamare [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), poiché in questo modo verranno cancellati i formati degli appunti che l'applicazione ha già eseguito il rendering.

Quando l'applicazione viene restituita, il sistema rimuove tutti i formati non sottoposto a rendering dall'elenco dei formati degli appunti disponibili. Per informazioni sul rendering ritardato, vedere [rendering ritardato](clipboard-operations.md#delayed-rendering).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



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

[**\_RENDERFORMAT WM**](wm-renderformat.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 

