---
title: Come fornire controlli Rich Edit senza finestra con la funzionalità finestra
description: La funzionalità finestra include la possibilità di ricevere messaggi e la proprietà di un contesto di dispositivo in cui eseguire il progetto. I controlli Rich Edit senza finestra ricevono questa funzionalità per mezzo di una coppia di interfacce ITextServices e ITextHost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce987630c21b1e15a2237066b39dd264125a857
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103956283"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a>Come fornire controlli Rich Edit senza finestra con la funzionalità finestra

La funzionalità finestra include la possibilità di ricevere messaggi e la proprietà di un contesto di dispositivo in cui eseguire il progetto. I controlli Rich Edit senza finestra ricevono questa funzionalità per mezzo di una coppia di interfacce: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="establish-the-window-functionality"></a>Definire la funzionalità della finestra

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

Il parametro *hmodRichEdit* nell'esempio di codice è un handle per il modulo Msftedit.dll e si presuppone che questo handle sia già stato recuperato da una chiamata alla funzione **GetModuleHandle** .

## <a name="complete-example"></a>Esempio completo

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit senza finestra](using-windowless-rich-edit-controls.md)
</dt> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




