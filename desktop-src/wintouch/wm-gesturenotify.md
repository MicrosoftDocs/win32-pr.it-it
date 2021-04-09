---
title: Messaggio WM_GESTURENOTIFY (winuser. h)
description: Offre la possibilità di impostare la configurazione dei movimenti.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY messaggio Windows Touch
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
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120338"
---
# <a name="wm_gesturenotify-message"></a>\_Messaggio GESTURENOTIFY WM

Offre la possibilità di impostare la configurazione dei movimenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un valore deve essere restituito da [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Quando viene ricevuto il messaggio **WM \_ GESTURENOTIFY** , l'applicazione può usare [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) per specificare i movimenti da ricevere. Questo messaggio deve essere sempre propagato tramite la funzione [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .

> [!Note]  
> La gestione del messaggio **WM \_ GESTURENOTIFY** modificherà la configurazione dei movimenti per la durata della finestra, non solo per il movimento successivo.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come abilitare tutti i movimenti. Per altri esempi, vedere [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Notifications](notifications.md)
</dt> <dt>

[Guida alla programmazione di movimenti tocco di Windows](guide-multi-touch-gestures.md)
</dt> <dt>

[**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

