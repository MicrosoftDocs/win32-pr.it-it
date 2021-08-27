---
title: Come usare le operazioni degli Appunti Rich Edit
description: Un'applicazione può incollare il contenuto degli Appunti in un controllo Rich Edit usando il formato degli Appunti migliore disponibile o un formato degli Appunti specifico.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdeac2e892716880e4e2971d597c13047dc79cebf2c57888e2fa248c6b0c4beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132091"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a>Come usare le operazioni degli Appunti Rich Edit

Un'applicazione può incollare il contenuto degli Appunti in un controllo Rich Edit usando il formato degli Appunti migliore disponibile o un formato degli Appunti specifico. È anche possibile determinare se un controllo Rich Edit è in grado di incollare un formato degli Appunti.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="use-a-rich-edit-clipboard-operation"></a>Usare un'operazione Degli Appunti Rich Edit

Come con un controllo di modifica, è possibile copiare o tagliare il contenuto della selezione corrente usando il messaggio [**\_ WM COPY**](/windows/desktop/dataxchg/wm-copy) o WM [**\_ CUT.**](/windows/desktop/dataxchg/wm-cut) Analogamente, è possibile incollare il contenuto degli Appunti in un controllo Rich Edit usando il [**messaggio \_ WM PASTE.**](/windows/desktop/dataxchg/wm-paste) Il controllo incolla il primo formato disponibile che riconosce, che presumibilmente è il formato più descrittivo.

Per incollare un formato degli Appunti specifico, è possibile usare il [**\_ messaggio EM PASTESPECIAL.**](em-pastespecial.md) Questo messaggio è utile per le applicazioni con **un comando Incolla** speciale che consente all'utente di selezionare il formato degli Appunti. È possibile usare il [**messaggio EM \_ CANPASTE**](em-canpaste.md) per determinare se un determinato formato viene riconosciuto dal controllo.

È anche possibile usare il [**messaggio EM \_ CANPASTE**](em-canpaste.md) per determinare se un formato degli Appunti disponibile viene riconosciuto da un controllo Rich Edit. Questo messaggio è utile quando si elabora [**il messaggio \_ WM INITMENUPOPUP.**](/windows/desktop/menurc/wm-initmenupopup) Un'applicazione potrebbe abilitare o disabilitare **il comando Incolla** a seconda che il controllo possa incollare qualsiasi formato disponibile.

I controlli Rich Edit registrano due formati degli Appunti:

-   Formato RTF (Rich Text Format)
-   Formato RTF senza oggetti
-   Testo e oggetti RichEdit

Un'applicazione può registrare questi formati usando la funzione [**RegisterClipboardFormat,**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) specificando i valori \_ CF RTF, \_ CF RTFNOOBJS e CF \_ RETEXTOBJ.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 