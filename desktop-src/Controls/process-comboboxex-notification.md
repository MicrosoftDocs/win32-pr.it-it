---
title: Come elaborare le notifiche ComboBoxEx
description: Questo argomento illustra come elaborare i messaggi di notifica ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ec73c31020283afe5876567a57fc1fbd8a23cee123e9dc417c14c57a86709a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575491"
---
# <a name="how-to-process-comboboxex-notifications"></a>Come elaborare le notifiche ComboBoxEx

Questo argomento illustra come elaborare i messaggi di notifica ComboBoxEx.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Un controllo ComboBoxEx invia una notifica alla finestra padre degli eventi inviando [**messaggi WM \_ NOTIFY.**](wm-notify.md) Passa anche i [**messaggi di notifica WM \_ COMMAND**](/windows/desktop/menurc/wm-command) ricevuti dalla casella combinata in essa contenuta alla finestra padre da elaborare. Pertanto, l'applicazione deve essere preparata a elaborare i messaggi **WM \_ NOTIFY** dai messaggi ComboBoxEx e **WM \_ COMMAND** inoltrati dal controllo casella combinata figlio ComboBoxEx.

L'esempio in questa sezione gestisce i messaggi [**WM \_ NOTIFY**](wm-notify.md) e [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) da un controllo ComboBoxEx chiamando una funzione corrispondente definita dall'applicazione per elaborare questi messaggi.

## <a name="complete-example"></a>Esempio completo


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Informazioni di riferimento sul controllo ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Uso dei controlli ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 