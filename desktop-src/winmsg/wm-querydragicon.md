---
description: Inviato a una finestra ridotta a icona (icona).
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: WM_QUERYDRAGICON messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20aac405a247f89a31c49f60a4e421fa171465d399dcb61a436936de5c646362
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055991"
---
# <a name="wm_querydragicon-message"></a>Messaggio \_ WM QUERYDRAGICON

Inviato a una finestra ridotta a icona (icona). La finestra sta per essere trascinata dall'utente, ma non ha un'icona definita per la relativa classe. Un'applicazione può restituire un handle a un'icona o a un cursore. Il sistema visualizza il cursore o l'icona mentre l'utente trascina l'icona.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Un'applicazione deve restituire un handle a un cursore o a un'icona che il sistema deve visualizzare mentre l'utente trascina l'icona. Il cursore o l'icona deve essere compatibile con la risoluzione del driver video. Se l'applicazione restituisce **NULL,** il sistema visualizza il cursore predefinito.

## <a name="remarks"></a>Commenti

Quando l'utente trascina l'icona di una finestra senza un'icona della classe, il sistema sostituisce l'icona con un cursore predefinito. Se l'applicazione richiede la visualizzazione di un cursore diverso durante il trascinamento, deve restituire un handle al cursore o all'icona compatibile con la risoluzione del driver di visualizzazione. Se un'applicazione restituisce un handle per un cursore o un'icona a colori, il sistema converte il cursore o l'icona in bianco e nero. L'applicazione può chiamare la [**funzione LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) o [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) per caricare un cursore o un'icona dalle risorse nel file eseguibile (.exe) e recuperare questo handle.

Se il messaggio viene gestito da una routine della finestra di dialogo, è necessario eseguire il cast del valore restituito desiderato in un valore **BOOL** e restituire direttamente il valore. Il **valore \_ MSGRESULT DWL** impostato dalla funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

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

[**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
