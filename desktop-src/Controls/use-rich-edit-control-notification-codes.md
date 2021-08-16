---
title: Come usare i codici di notifica del controllo Rich Edit
description: La finestra padre di un controllo Rich Edit può elaborare i codici di notifica per monitorare gli eventi che influiscono sul controllo. I controlli Rich Edit supportano tutti i codici di notifica usati con i controlli di modifica, oltre a diversi altri.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6bc730c648e76137db480f14895d540a9142ae6a80ffa58533e38ef513653ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828634"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a>Come usare i codici di notifica del controllo Rich Edit

La finestra padre di un controllo Rich Edit può elaborare i codici di notifica per monitorare gli eventi che influiscono sul controllo. I controlli Rich Edit supportano tutti i codici di notifica usati con i controlli di modifica, oltre a diversi altri.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="use-a-rich-edit-control-notification-code"></a>Usare un codice di notifica del controllo Rich Edit

È possibile determinare quali codici di notifica un controllo Rich Edit invia la finestra padre impostandone la maschera eventi. Per impostare la maschera eventi per un controllo Rich Edit, usare il [**messaggio EM \_ SETEVENTMASK.**](em-seteventmask.md) È possibile recuperare la maschera evento corrente per un controllo Rich Edit usando il [**messaggio EM \_ GETEVENTMASK.**](em-geteventmask.md) Per un elenco dei flag della maschera di evento, vedere [Flag di maschera eventi del](rich-edit-control-event-mask-flags.md)controllo Rich Edit .

La finestra padre di un controllo Rich Edit può filtrare tutto l'input da tastiera e mouse per il controllo elaborando il codice di notifica [EN \_ MSGFILTER.](en-msgfilter.md) La finestra padre può impedire l'elaborazione del messaggio della tastiera o del mouse oppure può modificare il messaggio modificando la struttura [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) specificata.

Un'applicazione può elaborare il codice di notifica [EN \_ PROTECTED](en-protected.md) per rilevare quando l'utente tenta di modificare il testo protetto. Per contrassegnare un intervallo di testo come protetto, è possibile impostare l'effetto carattere protetto.

È possibile abilitare l'utente per eliminare i file in un controllo Rich Edit elaborando il codice di notifica [EN \_ DROPFILES.](en-dropfiles.md) La struttura [**ENDROPFILES specificata**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) contiene informazioni sui file che vengono eliminati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




