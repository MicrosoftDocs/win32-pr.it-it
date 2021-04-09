---
title: Come utilizzare le operazioni Rich Edit Clipboard
description: Un'applicazione può incollare il contenuto degli Appunti in un controllo Rich Edit utilizzando il formato degli Appunti disponibile migliore o un formato degli Appunti specifico.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963505"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a>Come utilizzare le operazioni Rich Edit Clipboard

Un'applicazione può incollare il contenuto degli Appunti in un controllo Rich Edit utilizzando il formato degli Appunti disponibile migliore o un formato degli Appunti specifico. È inoltre possibile determinare se un controllo Rich Edit è in grado di incollare un formato degli Appunti.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-a-rich-edit-clipboard-operation"></a>Usa un'operazione Rich Edit Clipboard

Come con un controllo di modifica, è possibile copiare o tagliare il contenuto della selezione corrente usando il messaggio [**WM \_ Copy**](/windows/desktop/dataxchg/wm-copy) o [**WM \_ Cut**](/windows/desktop/dataxchg/wm-cut) . Analogamente, è possibile incollare il contenuto degli Appunti in un controllo Rich Edit usando il messaggio [**WM \_ paste**](/windows/desktop/dataxchg/wm-paste) . Il controllo incolla il primo formato disponibile che riconosce, che presumibilmente è il formato più descrittivo.

Per incollare un formato degli Appunti specifico, è possibile usare il messaggio [**\_ PASTESPECIAL em**](em-pastespecial.md) . Questo messaggio è utile per le applicazioni con un comando **Incolla speciale** che consente all'utente di selezionare il formato degli Appunti. È possibile usare il [**messaggio \_ CANPASTE em**](em-canpaste.md) per determinare se un formato specificato è riconosciuto dal controllo.

È anche possibile usare il [**messaggio \_ CANPASTE em**](em-canpaste.md) per determinare se un formato degli Appunti disponibile viene riconosciuto da un controllo Rich Edit. Questo messaggio è utile quando si elabora il messaggio [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) . Un'applicazione potrebbe abilitare o rendere grigio il comando **Incolla** a seconda che il controllo possa incollare qualsiasi formato disponibile.

I controlli Rich Edit registrano due formati degli Appunti:

-   Formato RTF
-   Formato RTF senza oggetti
-   Testo RichEdit e oggetti

Un'applicazione può registrare questi formati usando la funzione [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) , specificando i \_ valori CF RTF, CF \_ RTFNOOBJS e CF \_ RETEXTOBJ.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 