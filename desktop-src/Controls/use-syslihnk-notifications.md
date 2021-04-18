---
title: Come usare le notifiche SysLink
description: Sono presenti due messaggi di notifica associati al controllo SysLink \ 8212; uno per il mouse (NM \_ clic (Syslink)) e uno per la tastiera (Nm \_ Return).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "106299542"
---
# <a name="how-to-use-syslink-notifications"></a>Come usare le notifiche SysLink

Al controllo SysLink sono associati due messaggi di notifica: uno per il mouse ([nm \_ clic (Syslink)](nm-click-syslink.md)) e uno per la tastiera ([nm \_ return](nm-return.md)).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-syslink-notifications"></a>Usare le notifiche di SysLink

Nell'esempio di codice seguente viene illustrato come elaborare le notifiche SysLink generate quando l'utente fa clic su uno dei due collegamenti nell' [esempio precedente](create-syslink-controls.md). Quando l'utente fa clic sull'URL Internet, la pagina Web associata viene aperta nel browser predefinito. Quando l'utente fa clic sul collegamento ipertestuale definito dall'applicazione, viene visualizzata una finestra di messaggio.


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli SysLink](using-syslink-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




