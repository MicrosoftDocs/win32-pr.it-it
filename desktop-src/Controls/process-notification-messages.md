---
title: Come elaborare i messaggi di notifica
description: Una finestra delle proprietà invia messaggi WM NOTIFY per recuperare informazioni dalle pagine e \_ per notificare alle pagine le azioni dell'utente.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9baf0c58fdbcbe5378dd46e828a2d29a7c91832174c9564660a82c5ab70997a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575481"
---
# <a name="how-to-process-notification-messages"></a>Come elaborare i messaggi di notifica

Una finestra delle proprietà invia [**messaggi WM \_ NOTIFY**](wm-notify.md) per recuperare informazioni dalle pagine e per notificare alle pagine le azioni dell'utente.

Il *parametro lParam* del messaggio è l'indirizzo di una struttura [**NMHDR,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene l'handle per la finestra delle proprietà, l'handle per la finestra di dialogo della pagina e un codice di notifica. La pagina deve rispondere ad alcuni messaggi di notifica impostando il valore MSGRESULT DWL della pagina \_ su **TRUE** o **FALSE.**

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="process-notification-messages"></a>Elaborare i messaggi di notifica

L'esempio seguente è un frammento di codice della routine della finestra di dialogo per una pagina. Illustra come elaborare il codice [di notifica della \_ Guida di PSN.](psn-help.md)


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle finestre delle proprietà](using-property-sheets.md)
</dt> <dt>

[Windows demo di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




