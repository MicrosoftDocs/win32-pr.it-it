---
title: Come creare controlli Rich Edit
description: Per creare un controllo Rich Edit, chiamare la funzione CreateWindowEx, specificando la classe della finestra Rich Edit.
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047412"
---
# <a name="how-to-create-rich-edit-controls"></a>Come creare controlli Rich Edit

Per creare un controllo Rich Edit, chiamare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra Rich Edit. Per Microsoft Rich Edit 4,1 (Msftedit.dll), specificare \_ la classe MSFTEDIT come classe della finestra. Per tutte le versioni precedenti, specificare la classe RichEdit \_ . Per ulteriori informazioni, vedere [versioni di Rich Edit](about-rich-edit-controls.md).

I controlli Rich Edit supportano la maggior parte degli stili della finestra utilizzati con i controlli di modifica e altri stili. Se si desidera consentire più di una riga di testo nel controllo, è necessario specificare lo stile della finestra es su più [**\_ righe**](edit-control-styles.md) . Per altre informazioni, vedere [stili del controllo Rich Edit](rich-edit-control-styles.md).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="create-a-rich-edit-control"></a>Creazione di un controllo Rich Edit

La funzione di esempio seguente crea un controllo Rich Edit e lo inizializza con un testo.


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



In Microsoft Visual Studio 2005 e versioni successive, è possibile aggiungere un controllo Rich Edit in un modello di finestra di dialogo trascinando il controllo dalla casella degli strumenti. Tuttavia, l'operazione eseguita nell'editor finestre non garantisce che la libreria necessaria venga caricata prima della creazione del controllo. È necessario chiamare la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare Riched32.dll, Riched20.dll o Msftedit.dll prima della creazione della finestra di dialogo.

## <a name="remarks"></a>Commenti

Per usare gli stili di visualizzazione con questi controlli, un'applicazione deve includere un manifesto e deve chiamare la funzione [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) all'inizio del programma. Per informazioni sugli stili di visualizzazione, vedere [stili di visualizzazione](themes-overview.md). Per informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 