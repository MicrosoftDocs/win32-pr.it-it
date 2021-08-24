---
title: Come fornire controlli Rich Edit senza finestra con funzionalità finestra
description: La funzionalità finestra include la possibilità di ricevere messaggi e la proprietà di un contesto di dispositivo in cui disegnare. I controlli Rich Edit senza finestra ricevono questa funzionalità tramite una coppia di interfacce ITextServices e ITextHost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ce68a9e4e186be79e8f62cb009748916725e4af4f67d6522ed5eb47a92f33fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698601"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a>Come fornire controlli Rich Edit senza finestra con funzionalità finestra

La funzionalità finestra include la possibilità di ricevere messaggi e la proprietà di un contesto di dispositivo in cui disegnare. I controlli Rich Edit senza finestra ricevono questa funzionalità tramite una coppia di interfacce: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e [**ITextHost.**](/windows/desktop/api/Textserv/nl-textserv-itexthost)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="establish-the-window-functionality"></a>Stabilire la funzionalità della finestra

Nell'esempio di codice seguente viene illustrato come creare l'host di testo e i servizi di testo.


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a>Commenti

Il *parametro hmodRichEdit* nell'esempio di codice è un handle per il modulo Msftedit.dll e si presuppone che questo handle sia già stato recuperato da una chiamata alla **funzione GetModuleHandle.**

## <a name="complete-example"></a>Esempio completo

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit senza finestra](using-windowless-rich-edit-controls.md)
</dt> <dt>

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




