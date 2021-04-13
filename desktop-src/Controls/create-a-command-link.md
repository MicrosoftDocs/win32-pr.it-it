---
title: Come creare un collegamento di comando
description: In questo argomento viene descritto un modo per creare un collegamento di comando.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8024a7f060a7bae3779b9ec9ebec40bd81c74bb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474462"
---
# <a name="how-to-create-a-command-link"></a>Come creare un collegamento di comando

In questo argomento viene descritto un modo per creare un collegamento di comando.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-an-instance-of-the-command-link-button"></a>Passaggio 1: creare un'istanza del pulsante di collegamento al comando.

Nell'esempio di codice C++ riportato di seguito, la costante di stile [**BS \_ COMMANDLINK**](button-styles.md) specifica il pulsante come pulsante di collegamento del comando.


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a>Passaggio 2: impostare l'etichetta del collegamento del comando e il testo della spiegazione

Utilizzare la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per impostare l'etichetta del collegamento del comando e il testo supplementare rispettivamente tramite il messaggio [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) e il messaggio di [**\_ Nota BCM**](bcm-setnote.md) .


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui pulsanti](about-buttons.md)
</dt> <dt>

[Riferimento al controllo Button](bumper-button-button-control-reference.md)
</dt> <dt>

[Uso di pulsanti](using-buttons.md)
</dt> <dt>

[Button](buttons.md)
</dt> </dl>

 

 