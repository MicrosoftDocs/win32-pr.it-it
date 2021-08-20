---
title: Come usare i metodi tab in TOM
description: Nell'esempio seguente vengono fornite funzioni C che illustrano l'uso dei metodi tab nel modello a oggetti di testo (TOM, Text Object Model).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b4a101c2deb3c22993f41b11ee94df6ac738da41963046f02a072f3eaa6a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828613"
---
# <a name="how-to-use-tab-methods-in-tom"></a>Come usare i metodi tab in TOM

Nell'esempio seguente vengono fornite funzioni C che illustrano l'uso dei metodi tab nel modello a oggetti di testo (TOM, Text Object Model). Si presuppone che la maggior parte delle applicazioni includa una barra degli strumenti che mostra la posizione e il tipo correnti delle schede per il paragrafo attualmente selezionato.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="use-a-tab-method"></a>Usare un metodo Tab

Nell'esempio di codice seguente viene illustrato come aggiornare una barra degli strumenti con i dettagli della scheda corrente.


```C++
HRESULT UpdateToolbar(ITextSelection *pSel)
{
    HRESULT hr       = S_OK;        
    ITextPara *pPara = 0;
    
    float f;
    long tbt;            // tab type
    long tbp;

    hr = pSel->GetPara(&pPara);
    
    if (FAILED(hr))
        goto cleanup;    // Paragraph properties are not supported
    
    f = (float) -1.0;    // Start at beginning
    
    while (pPara->GetTab(tbgoNext, &f, &tbt, NULL) == S_OK)
    {
            // Do something like draw tab icon on toolbar here
            // DrawTabPicture(f, tbt);
    }
    
cleanup:

    if (pPara)
        pPara->Release();
        
    return hr;
    
}
```



### <a name="copy-tab-information"></a>Copia informazioni scheda

L'esempio seguente illustra come copiare solo le informazioni sulla scheda da [**un'interfaccia ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) a un'altra. Accetta due parametri: **ITextPara** pParaFrom (il paragrafo da cui copiare le tabulazioni) e \*  **ITextPara** \* *pParaFrom* (il paragrafo in cui copiare le tabulazioni).


```C++
HRESULT CopyOnlyTabs(ITextPara *pParaFrom, ITextPara *pParaTo)
{
    float f;
    short tbt;
    short style;
     
    pParaTo->ClearAllTabs();
    
    f = (float) -1.0;
    
    while (pParaFrom->GetTab(tbgoNext, &f, &tbt, &style) == S_OK)
        pParaTo->AddTab(f, tbt, style);
        
    return S_OK;                
    
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del modello a oggetti di testo](using-the-text-object-model.md)
</dt> <dt>

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




