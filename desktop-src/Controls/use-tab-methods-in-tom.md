---
title: Come usare i metodi di tabulazione in TOM
description: Nell'esempio seguente vengono fornite le funzioni C che illustrano l'utilizzo dei metodi di tabulazione nel modello a oggetti di testo (TOM).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9851b30fdf58c0d4200600c0c4c83c7f9a00a555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103872227"
---
# <a name="how-to-use-tab-methods-in-tom"></a>Come usare i metodi di tabulazione in TOM

Nell'esempio seguente vengono fornite le funzioni C che illustrano l'utilizzo dei metodi di tabulazione nel modello a oggetti di testo (TOM). Si presuppone che la maggior parte delle applicazioni includa una barra degli strumenti che mostra la posizione corrente e il tipo delle schede per il paragrafo attualmente selezionato.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-a-tab-method"></a>Usare un metodo Tab

Nell'esempio di codice riportato di seguito viene illustrato come aggiornare una barra degli strumenti con i dettagli della scheda corrente.


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

Nell'esempio seguente viene illustrato come copiare solo le informazioni di tabulazione da un'interfaccia [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) a un'altra. Accetta due parametri: **ITextPara** \* *pParaFrom* (il paragrafo da cui copiare le schede) e **ITextPara** \* *pParaFrom* (il paragrafo in cui copiare le schede).


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

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




