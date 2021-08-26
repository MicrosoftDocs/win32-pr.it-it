---
title: Come etichettare dinamicamente i pulsanti della barra degli strumenti
description: È possibile assegnare testo a un pulsante esistente usando il messaggio \_ TB SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063a3b8be8a23dc8cead219c53989a8ff1a40225dc8411f9e8a1b156b6bb55bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877441"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Come etichettare dinamicamente i pulsanti della barra degli strumenti

È possibile assegnare testo a un pulsante esistente usando il [**messaggio \_ TB SETBUTTONINFO.**](tb-setbuttoninfo.md)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="dynamically-label-a-toolbar-button"></a>Etichettare dinamicamente un pulsante della barra degli strumenti

Nell'esempio seguente viene illustrato come modificare il testo del terzo pulsante negli esempi precedenti da **Salva** **in Salva con nome**.


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

La modifica del testo di un pulsante tramite [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) non influisce sulla stringa assegnata a tale pulsante nell'elenco di stringhe interno.

Se si aggiunge una stringa del pulsante della barra degli strumenti all'elenco di testo interno, non è possibile recuperare l'indice di tale stringa chiamando [TBN \_ GETBUTTONINFO.](tbn-getbuttoninfo.md)È invece necessario usare il messaggio [**TB \_ GETBUTTON.**](tb-getbutton.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli barra degli strumenti](using-toolbar-controls.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




