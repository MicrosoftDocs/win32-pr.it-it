---
title: Come etichettare dinamicamente i pulsanti della barra degli strumenti
description: È possibile assegnare testo a un pulsante esistente usando il messaggio TB \_ SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "104472427"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Come etichettare dinamicamente i pulsanti della barra degli strumenti

È possibile assegnare testo a un pulsante esistente usando il messaggio [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) .

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="dynamically-label-a-toolbar-button"></a>Etichetta dinamicamente un pulsante della barra degli strumenti

Nell'esempio seguente viene illustrato come modificare il testo del terzo pulsante degli esempi precedenti da **Save** in Salva con **nome**.


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a>Commenti

La modifica del testo di un pulsante con [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) non influisce sulla stringa assegnata a tale pulsante nell'elenco di stringhe interno.

Se si aggiunge una stringa del pulsante della barra degli strumenti all'elenco di testo interno, non è possibile recuperare l'indice di tale stringa chiamando [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md): è necessario usare invece il messaggio [**TB \_ GetButton**](tb-getbutton.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di controlli Toolbar](using-toolbar-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




