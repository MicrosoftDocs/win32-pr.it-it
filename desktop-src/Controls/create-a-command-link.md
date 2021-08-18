---
title: Come creare un collegamento a un comando
description: In questo argomento viene descritto un modo per creare un collegamento di comando.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c61888921f06e017ec1ea625730c3cc52de5ab364db22fc01fd021ce5629c63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920901"
---
# <a name="how-to-create-a-command-link"></a>Come creare un collegamento a un comando

In questo argomento viene descritto un modo per creare un collegamento di comando.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-an-instance-of-the-command-link-button"></a>Passaggio 1: Creare un'istanza del pulsante di collegamento al comando.

Nell'esempio di codice C++ seguente la costante di stile [**BS \_ COMMANDLINK**](button-styles.md) specifica il pulsante come pulsante di collegamento di comando.


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



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a>Passaggio 2: Impostare l'etichetta del collegamento al comando e il testo della spiegazione

Usare la [**funzione SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per impostare l'etichetta del collegamento al comando e il testo supplementare rispettivamente tramite il messaggio [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) e il messaggio [**\_ BCM SETNOTE.**](bcm-setnote.md)


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui pulsanti](about-buttons.md)
</dt> <dt>

[Informazioni di riferimento sul controllo Button](bumper-button-button-control-reference.md)
</dt> <dt>

[Uso dei pulsanti](using-buttons.md)
</dt> <dt>

[Button](buttons.md)
</dt> </dl>

 

 