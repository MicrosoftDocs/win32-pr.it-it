---
description: Inviato a una finestra ridotta a icona.
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: Messaggio WM_QUERYDRAGICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345581"
---
# <a name="wm_querydragicon-message"></a>\_Messaggio QUERYDRAGICON WM

Inviato a una finestra ridotta a icona. La finestra sta per essere trascinata dall'utente, ma non dispone di un'icona definita per la relativa classe. Un'applicazione può restituire un handle per un'icona o un cursore. Il sistema Visualizza il cursore o l'icona quando l'utente trascina l'icona.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_QUERYDRAGICON                0x0037
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

Un'applicazione deve restituire un handle a un cursore o a un'icona visualizzata dal sistema mentre l'utente trascina l'icona. Il cursore o l'icona deve essere compatibile con la risoluzione del driver di visualizzazione. Se l'applicazione restituisce **null**, il sistema Visualizza il cursore predefinito.

## <a name="remarks"></a>Commenti

Quando l'utente trascina l'icona di una finestra senza un'icona di classe, il sistema sostituisce l'icona con un cursore predefinito. Se l'applicazione richiede la visualizzazione di un cursore diverso durante il trascinamento, deve restituire un handle per il cursore o l'icona compatibile con la risoluzione del driver visualizzato. Se un'applicazione restituisce un handle a un cursore o a un'icona di colore, il sistema converte il cursore o l'icona in bianco e nero. L'applicazione può chiamare la funzione [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) o [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) per caricare un cursore o un'icona dalle risorse nel file eseguibile (exe) e recuperare questo handle.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **bool** e restituire direttamente il valore. Il valore **DWL \_ MSGRESULT** impostato dalla funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

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

[**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
