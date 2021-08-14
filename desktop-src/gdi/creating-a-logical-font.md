---
description: È possibile usare la finestra di dialogo Tipo di carattere comune per visualizzare i tipi di carattere disponibili.
ms.assetid: 317ea311-0592-432a-87b5-58296de003aa
title: Creazione di un tipo di carattere logico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb491a1af055963053e8b0247ecaa212547a750a7bd0a35db0ae983695a2420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887471"
---
# <a name="creating-a-logical-font"></a>Creazione di un tipo di carattere logico

È possibile usare la finestra **di dialogo Tipo** di carattere comune per visualizzare i tipi di carattere disponibili. La **finestra di dialogo ChooseFont** viene visualizzata dopo che un'applicazione inizializza i membri di una struttura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) e chiama la [**funzione CHOOSEFONT.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) Dopo che l'utente ha selezionato uno dei tipi di carattere disponibili e ha premuto il pulsante **OK,** la funzione **ChooseFont** inizializza una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) con i dati pertinenti. L'applicazione può quindi chiamare la [**funzione CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta) e creare un tipo di carattere logico in base alla richiesta dell'utente. Nell'esempio seguente viene illustrato come eseguire questa operazione.


```C++
HFONT FAR PASCAL MyCreateFont( void ) 
{ 
    CHOOSEFONT cf; 
    LOGFONT lf; 
    HFONT hfont; 
 
    // Initialize members of the CHOOSEFONT structure.  
 
    cf.lStructSize = sizeof(CHOOSEFONT); 
    cf.hwndOwner = (HWND)NULL; 
    cf.hDC = (HDC)NULL; 
    cf.lpLogFont = &lf; 
    cf.iPointSize = 0; 
    cf.Flags = CF_SCREENFONTS; 
    cf.rgbColors = RGB(0,0,0); 
    cf.lCustData = 0L; 
    cf.lpfnHook = (LPCFHOOKPROC)NULL; 
    cf.lpTemplateName = (LPSTR)NULL; 
    cf.hInstance = (HINSTANCE) NULL; 
    cf.lpszStyle = (LPSTR)NULL; 
    cf.nFontType = SCREEN_FONTTYPE; 
    cf.nSizeMin = 0; 
    cf.nSizeMax = 0; 
 
    // Display the CHOOSEFONT common-dialog box.  
 
    ChooseFont(&cf); 
 
    // Create a logical font based on the user's  
    // selection and return a handle identifying  
    // that font.  
 
    hfont = CreateFontIndirect(cf.lpLogFont); 
    return (hfont); 
} 
```



 

 
