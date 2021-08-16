---
title: WM_GESTURENOTIFY messaggio (Winuser.h)
description: Consente di impostare la configurazione del movimento.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY messaggio Windows Tocco
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d474f356310a0d7949cecf36e7af9cb586a76029171dfe27c1679970e481ed1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435237"
---
# <a name="wm_gesturenotify-message"></a>Messaggio WM \_ GESTURENOTIFY

Consente di impostare la configurazione del movimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**UN GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un valore deve essere restituito [da DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Quando viene **ricevuto il messaggio WM \_ GESTURENOTIFY,** l'applicazione può usare [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) per specificare i movimenti da ricevere. Questo messaggio deve sempre essere visualizzato tramite la [funzione DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca)

> [!Note]  
> La gestione **del messaggio WM \_ GESTURENOTIFY** modificherà la configurazione del movimento per la durata della finestra, non solo per il movimento successivo.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come abilitare tutti i movimenti. Per altri esempi, vedere [**SetGestureConfig.**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Notifications](notifications.md)
</dt> <dt>

[Windows Guida alla programmazione dei movimenti tocco](guide-multi-touch-gestures.md)
</dt> <dt>

[**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

