---
title: Come creare controlli SysLink
description: I collegamenti ipertestuali del controllo SysLink vengono implementati attraverso il markup nella stringa di inizializzazione del controllo oppure tramite l'invio di un \_ messaggio di elemento.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa5c5ff3348f35f9c67cb34bea0cc495d403ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730655"
---
# <a name="how-to-create-syslink-controls"></a>Come creare controlli SysLink

I collegamenti ipertestuali del controllo SysLink vengono implementati attraverso il markup nella stringa di inizializzazione del controllo oppure tramite l'invio di un messaggio di [**\_ elemento**](lm-setitem.md) .

> [!Note]  
> Prima di creare controlli SysLink, è necessario chiamare la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , specificando la \_ classe di collegamento ICC \_ .

 

Per creare un SysLink, chiamare la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra di [**\_ collegamento WC**](common-control-window-classes.md) . Il parametro *lpWindowName* comune a queste funzioni specifica un puntatore a una stringa con terminazione zero che contiene il testo contrassegnato per la visualizzazione. Per gli stili della finestra specifici dei controlli SysLink, vedere [stili di controllo Syslink](syslink-control-styles.md).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

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

Specificando lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) si garantisce che l'utente sia in grado di selezionare un collegamento tramite tabulazione e premendo il tasto INVIO.

La versione 6 di ComCtl32.dll supporta solo Unicode. Pertanto, non è possibile creare versioni ANSI dei controlli SysLink, solo Unicode.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli SysLink](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 