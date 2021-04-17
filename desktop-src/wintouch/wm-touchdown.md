---
title: Messaggio WM_TOUCH (winuser. h)
description: Notifica alla finestra quando uno o più punti di tocco, ad esempio un dito o una penna, tocca una superficie del digitalizzatore sensibile al tocco.
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
ms.openlocfilehash: 6b6242d43b661240d946d2883237640d1bc92b3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400763"
---
# <a name="wm_touch-message"></a>\_Messaggio WM touch

Notifica alla finestra quando uno o più punti di tocco, ad esempio un dito o una penna, tocca una superficie del digitalizzatore sensibile al tocco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine inferiore contiene il numero di punti di tocco associati a questo messaggio. La parola più ordinata è riservata per un utilizzo futuro.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene un handle di input tocco che può essere utilizzato in una chiamata a [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) per recuperare informazioni dettagliate sui punti di tocco associati a questo messaggio.

Questo handle è valido solo all'interno del processo corrente e non deve essere passato tra processi, ad eccezione di **lParam** in una chiamata **SendMessage** o **PostMessage** .

Quando l'applicazione non richiede più questo handle, l'applicazione deve chiamare **CloseTouchInputHandle** per liberare la memoria del processo associata a questo handle. In caso contrario, può verificarsi una perdita di memoria dell'applicazione.

Si noti che l'handle di input tocco in questo parametro non è più valido dopo che il messaggio è stato passato a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) si chiude e invalida questo handle.

Si noti inoltre che l'handle di input tocco in questo parametro non è più valido dopo che il messaggio è stato inviato tramite [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage** o una delle relative varianti. Queste funzioni chiudono e invalideranno questo handle.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

Se l'applicazione non elabora il messaggio, deve chiamare [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Se non si esegue questa operazione, l'applicazione perde memoria perché l'handle di input tocco non è chiuso e la memoria del processo associata non viene liberata.

## <a name="remarks"></a>Commenti

**WM \_** I messaggi touch non rispettano le aree **HTTRANSPARENT** di Windows. Se una finestra restituisce **HTTRANSPARENT** in risposta a un messaggio **WM \_ NCHITTEST** , i messaggi del mouse passano al padre e i messaggi **WM \_ touch** passano direttamente alla finestra.

## <a name="examples"></a>Esempio

Il codice seguente è un esempio di come ottenere informazioni dettagliate sull'input di tocco associate a questo messaggio.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> <dt>

[Guida alla programmazione di modifiche e inerzia](manipulation-and-inertia.md)
</dt> <dt>

[Guida alla programmazione di input per Windows Touch](guide-multi-touch-input.md)
</dt> </dl>

 

