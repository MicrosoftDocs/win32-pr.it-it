---
title: Come utilizzare i codici di notifica del controllo Rich Edit
description: Una finestra padre di un controllo Rich Edit può elaborare i codici di notifica per monitorare gli eventi che influiscono sul controllo. I controlli Rich Edit supportano tutti i codici di notifica utilizzati con i controlli di modifica, oltre a diversi altri.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103956287"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a>Come utilizzare i codici di notifica del controllo Rich Edit

Una finestra padre di un controllo Rich Edit può elaborare i codici di notifica per monitorare gli eventi che influiscono sul controllo. I controlli Rich Edit supportano tutti i codici di notifica utilizzati con i controlli di modifica, oltre a diversi altri.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-a-rich-edit-control-notification-code"></a>Usare un codice di notifica del controllo Rich Edit

È possibile individuare i codici di notifica che un controllo Rich Edit Invia la finestra padre impostando la relativa maschera eventi. Per impostare la maschera eventi per un controllo Rich Edit, utilizzare il [**messaggio \_ SETEVENTMASK em**](em-seteventmask.md) . È possibile recuperare la maschera eventi corrente per un controllo Rich Edit usando il messaggio [**\_ GETEVENTMASK em**](em-geteventmask.md) . Per un elenco di flag di maschera eventi, vedere [flag di maschera eventi del controllo Rich Edit](rich-edit-control-event-mask-flags.md).

Una finestra padre di un controllo Rich Edit può filtrare tutti gli input di tastiera e mouse nel controllo elaborando il codice di notifica [en \_ msgfilter](en-msgfilter.md) . La finestra padre può impedire l'elaborazione del messaggio della tastiera o del mouse oppure può modificare il messaggio modificando la struttura [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) specificata.

Un'applicazione può elaborare il codice di notifica [ \_ protetto it](en-protected.md) per rilevare quando l'utente tenta di modificare il testo protetto. Per contrassegnare un intervallo di testo come protetto, è possibile impostare l'effetto carattere protetto.

È possibile consentire all'utente di eliminare i file in un controllo Rich Edit elaborando il codice di notifica [en \_ DropFiles](en-dropfiles.md) . La struttura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) specificata contiene informazioni sui file che vengono eliminati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




