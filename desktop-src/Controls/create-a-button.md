---
title: Come creare un pulsante
description: Per creare pulsanti in modo dinamico, usare la funzione CreateWindow o CreateWindowEx. In questo argomento viene illustrato come utilizzare la funzione CreateWindow per creare un pulsante di push predefinito.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047624"
---
# <a name="how-to-create-a-button"></a>Come creare un pulsante

Per creare pulsanti in modo dinamico, usare la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . In questo argomento viene illustrato come utilizzare la funzione **CreateWindow** per creare un pulsante di push predefinito.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Usare la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) per creare un controllo Button.

Nel seguente esempio di C++, il *parametro \_ HWND m* è l'handle per la finestra padre. Lo stile [**BS \_ DEFPUSHBUTTON**](button-styles.md) specifica che deve essere creato un pulsante di push predefinito. Si noti che è necessario specificare i valori delle dimensioni e della posizione perché l'uso di **CW \_ usedefault (** per un pulsante Imposta i valori su zero.


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
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

 

 