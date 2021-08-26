---
title: Come ridimensionare automaticamente i controlli Rich Edit
description: Un'applicazione può ridimensionare un controllo Rich Edit in base alle esigenze in modo che sia sempre delle stesse dimensioni del relativo contenuto.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef3fa798da0a7747464d42535c638f437154124dd76b0324add35b5ba01931a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921721"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a>Come ridimensionare automaticamente i controlli Rich Edit

Un'applicazione può ridimensionare un controllo Rich Edit in base alle esigenze in modo che sia sempre delle stesse dimensioni del relativo contenuto. Un controllo Rich Edit supporta  questa cosiddetta funzionalità senza fondo inviando alla finestra padre un codice di notifica [EN \_ REQUESTRESIZE](en-requestresize.md) ogni volta che le dimensioni del contenuto del controllo cambiano.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="automatically-resize-a-rich-edit-control"></a>Ridimensionare automaticamente un controllo Rich Edit

Durante l'elaborazione del codice di notifica [EN \_ REQUESTRESIZE,](en-requestresize.md) un'applicazione deve ridimensionare il controllo in base alle dimensioni nella struttura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) specificata. Un'applicazione potrebbe anche spostare le informazioni vicine al controllo per adattare la modifica dell'altezza del controllo. Per ridimensionare il controllo, puoi usare la [**funzione SetWindowPos.**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)

È possibile forzare un controllo rich edit senza fondo a inviare un codice di notifica [EN \_ REQUESTRESIZE](en-requestresize.md) usando il [**messaggio EM \_ REQUESTRESIZE.**](em-requestresize.md) Questo messaggio può essere utile durante l'elaborazione del [**messaggio WM \_ SIZE.**](/windows/desktop/winmsg/wm-size)

## <a name="remarks"></a>Commenti

Per ricevere [i codici di notifica EN \_ REQUESTRESIZE,](en-requestresize.md) è necessario abilitare la notifica usando il [messaggio EM \_ SETEVENTMASK.](em-seteventmask.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 