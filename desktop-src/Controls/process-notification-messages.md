---
title: Come elaborare i messaggi di notifica
description: Una finestra delle proprietà Invia \_ messaggi WM Notify per recuperare le informazioni dalle pagine e per notificare le pagine delle azioni dell'utente.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724275"
---
# <a name="how-to-process-notification-messages"></a>Come elaborare i messaggi di notifica

Una finestra delle proprietà Invia messaggi [**WM \_ Notify**](wm-notify.md) per recuperare le informazioni dalle pagine e per notificare le pagine delle azioni dell'utente.

Il parametro *lParam* del messaggio è l'indirizzo di una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , che contiene l'handle per la finestra di dialogo della finestra delle proprietà, l'handle per la finestra di dialogo della pagina e un codice di notifica. La pagina deve rispondere ad alcuni messaggi di notifica impostando il \_ valore DWL MSGRESULT della pagina su **true** o **false**.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="process-notification-messages"></a>Elaborare i messaggi di notifica

Nell'esempio seguente è riportato un frammento di codice della routine della finestra di dialogo per una pagina. Viene illustrato come elaborare il codice di notifica della [ \_ Guida di PSN](psn-help.md) .


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

[Utilizzo delle finestre delle proprietà](using-property-sheets.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




