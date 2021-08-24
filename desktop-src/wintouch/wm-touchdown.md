---
title: WM_TOUCH messaggio (Winuser.h)
description: Notifica alla finestra quando uno o più punti tocco, ad esempio un dito o una penna, toccano una superficie del digitalizzatore sensibile al tocco.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- WM_TOUCH messaggio Windows Touch
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1034a229dbb1f3895726fcb3c1551e2dd0f390be0fd7bc2eb81d8331e582eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810101"
---
# <a name="wm_touch-message"></a>Messaggio WM \_ TOUCH

Notifica alla finestra quando uno o più punti tocco, ad esempio un dito o una penna, toccano una superficie del digitalizzatore sensibile al tocco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine basso contiene il numero di punti di tocco associati a questo messaggio. La parola di ordine alto è riservata per un uso futuro.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene un handle di input tocco che può essere usato in una chiamata a [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) per recuperare informazioni dettagliate sui punti di tocco associati a questo messaggio.

Questo handle è valido solo all'interno del processo corrente e non deve essere passato tra processi tranne che come **LPARAM** in una **chiamata SendMessage** **o PostMessage.**

Quando l'applicazione non richiede più questo handle, l'applicazione deve chiamare **CloseTouchInputHandle** per liberare la memoria del processo associata a questo handle. In caso negativo, può verificarsi una perdita di memoria dell'applicazione.

Si noti che l'handle di input tocco in questo parametro non è più valido dopo che il messaggio è stato passato a [DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca) [DefWindowProc chiuderà](/windows/win32/api/winuser/nf-winuser-defwindowproca) e invaliderà questo handle.

Si noti anche che l'handle di input tocco in questo parametro non è più valido dopo l'inoltro del messaggio tramite [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage** o una delle relative varianti. Queste funzioni chiuderanno e invalideranno questo handle.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

Se l'applicazione non elabora il messaggio, deve chiamare [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). In questo modo l'applicazione perde memoria perché l'handle di input tocco non viene chiuso e la memoria del processo associata non viene liberata.

## <a name="remarks"></a>Commenti

**WM \_ I** messaggi TOUCH non rispettano **le aree HTTRANSPARENT** delle finestre. Se una finestra restituisce **HTTRANSPARENT** in risposta a un messaggio **WM \_ NCHITTEST,** i messaggi del mouse passano all'elemento padre e i messaggi **WM \_ TOUCH** passano direttamente alla finestra.

## <a name="examples"></a>Esempio

Il codice seguente è un esempio di come ottenere informazioni dettagliate sull'input tocco associate a questo messaggio.


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> <dt>

[Guida per programmatori Manipolazioni e inerzia](manipulation-and-inertia.md)
</dt> <dt>

[Windows Guida alla programmazione dell'input tocco](guide-multi-touch-input.md)
</dt> </dl>

 

