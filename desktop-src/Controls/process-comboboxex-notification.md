---
title: Come elaborare le notifiche ComboBoxEx
description: In questo argomento viene illustrato come elaborare i messaggi di notifica ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963604"
---
# <a name="how-to-process-comboboxex-notifications"></a>Come elaborare le notifiche ComboBoxEx

In questo argomento viene illustrato come elaborare i messaggi di notifica ComboBoxEx.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Un controllo ComboBoxEx notifica la finestra padre degli eventi inviando i messaggi di [**\_ notifica WM**](wm-notify.md) . Passa inoltre i messaggi di notifica dei [**\_ comandi WM**](/windows/desktop/menurc/wm-command) ricevuti dalla casella combinata contenuta al suo interno alla finestra padre da elaborare. Pertanto, l'applicazione deve essere preparata per l'elaborazione dei messaggi di **\_ notifica WM** dai messaggi di **\_ comando** ComboBoxEx e WM che vengono inviati dal controllo casella combinata figlio ComboBoxEx.

Nell'esempio riportato in questa sezione vengono gestiti i messaggi [**WM \_ Notify**](wm-notify.md) e [**WM \_ Command**](/windows/desktop/menurc/wm-command) da un controllo ComboBoxEx tramite una chiamata a una funzione definita dall'applicazione corrispondente per elaborare questi messaggi.

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

[Riferimento al controllo ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Uso di controlli ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 