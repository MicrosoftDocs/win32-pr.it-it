---
title: Come creare controlli SysLink
description: I collegamenti ipertestuali del controllo SysLink vengono implementati tramite markup nella stringa di inizializzazione del controllo o inviando un messaggio \_ LM SETITEM.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2b50e364a2701d52aa0ed62222b0901a66b6c4073891b7f9348fffc8997fdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878511"
---
# <a name="how-to-create-syslink-controls"></a>Come creare controlli SysLink

I collegamenti ipertestuali del controllo SysLink vengono implementati tramite markup nella stringa di inizializzazione del controllo o inviando un [**messaggio \_ LM SETITEM.**](lm-setitem.md)

> [!Note]  
> Prima di creare controlli SysLink, è necessario chiamare [**la funzione InitCommonControlsEx,**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) specificando la classe ICC \_ \_ LINK.

 

Per creare un syslink, chiamare la [**funzione CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) specificando la classe di finestra [**WC \_ LINK.**](common-control-window-classes.md) Il *parametro lpWindowName* comune a queste funzioni specifica un puntatore a una stringa con terminazione zero che contiene il testo contrassegnato da visualizzare. Per gli stili delle finestre specifici dei controlli SysLink, vedere [Stili del controllo SysLink.](syslink-control-styles.md)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="create-a-syslink-control"></a>Creare un controllo SysLink

Il codice di esempio seguente crea un controllo SysLink che visualizza due collegamenti ipertestuali. Il primo collegamento ipertestuale è un URL Internet e il secondo è definito dall'applicazione.


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a>Commenti

Si presuppone che [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) sia già stato chiamato.

Se si specifica [**lo stile WS \_ TABSTOP,**](/windows/desktop/winmsg/window-styles) l'utente potrà selezionare un collegamento premendo TAB.

La versione 6 ComCtl32.dll supporta solo Unicode. Pertanto, non è possibile creare versioni ANSI dei controlli SysLink, ma solo Unicode.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli SysLink](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

[Windows demo di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 