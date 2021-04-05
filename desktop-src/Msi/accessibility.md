---
description: Quando si progettano l'interfaccia utente in modo che siano conformi alle linee guida Active Accessibility, gli autori devono tenere presenti le tabelle e i campi nell'elenco seguente.
ms.assetid: 516e504e-7895-4388-a38e-fd2fc7dfd61d
title: Accessibilità (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46325c11337ef1e1db6f2da5728f06f9d4ee0649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881173"
---
# <a name="accessibility-windows-installer"></a>Accessibilità (Windows Installer)

Quando si progettano l'interfaccia utente in modo che siano conformi alle linee guida Active Accessibility, gli autori devono tenere presenti le tabelle e i campi nell'elenco seguente. L'interfaccia utente di un pacchetto di installazione deve facilitare l'accessibilità dell'applicazione o del prodotto a tutti gli utenti.

-   Il testo della descrizione comando è contenuto nella colonna guida della [tabella dei controlli](control-table.md). Questo testo viene visualizzato dalle utilità per la lettura dello schermo per i controlli che contengono un'immagine.
-   Il campo di testo della [tabella di controllo](control-table.md) per i controlli [VolumeCostList](volumecostlist-control.md), [ListView](listview-control.md), [directory](directorylist-control.md) e [SelectionTree](selectiontree-control.md) non viene mai visualizzato. In alternativa, è possibile leggere le utilità di revisione dello schermo come descrizione del controllo. Gli utenti che non possono utilizzare le informazioni visive sullo schermo possono interpretare le informazioni con l'ausilio di un'utilità di analisi dello schermo. Le utilità di analisi dello schermo, dette anche programmi per la lettura dello schermo o utilità di accesso vocale, accettano le informazioni visualizzate sullo schermo e le indirizzano attraverso supporti alternativi, ad esempio sintesi vocale sintetizzata o una visualizzazione Braille aggiornabile.
-   I controlli nelle finestre di dialogo devono essere collegati utilizzando il \_ campo controllo successivo della [tabella dei controlli](control-table.md). È necessario creare i controlli in modo che possano essere tutti raggiunti utilizzando il tasto TAB.
-   È necessario fornire i tasti di scelta rapida per accedere direttamente ai controlli.
-   Il colore del testo visualizzato nell'interfaccia utente è impostato nella [tabella TextStyle](textstyle-table.md). Se il colore del testo scelto è troppo vicino allo sfondo, la scelta del colore del testo viene ignorata.
-   Le dimensioni del testo e il tipo di carattere sono impostati nella [tabella TextStyle](textstyle-table.md). Per i pacchetti destinati al mercato asiatico, è necessario utilizzare dimensioni maggiori per i tipi di carattere. Ad esempio, le dimensioni del carattere pari a 10 punti leggibili per il testo in inglese potrebbero non essere necessariamente vere per il cinese.
-   Per i controlli [Edit](edit-control.md), [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) o [VolumeSelectCombo](volumeselectcombo-control.md), le utilità per la lettura dello schermo accettano accName e accKeyboardShortcut da un [controllo di testo](text-control.md) che deve precedere il controllo nella \_ sequenza successiva del controllo della finestra di dialogo. L'Reader per la lettura dello schermo accetta accName dal campo di testo del controllo testo e accKeyboardShortcut dal tasto di scelta rapida nel campo di testo, se è presente un collegamento.
-   Poiché il testo statico non può avere lo stato attivo, un [controllo di testo](text-control.md) che descrive un controllo [Edit](edit-control.md), [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) o [VolumeSelectCombo](volumeselectcombo-control.md) deve essere reso il primo controllo nella finestra di dialogo per garantire la compatibilità con le utilità per la lettura dello schermo.
-   Per un [controllo pulsante](pushbutton-control.md) che visualizza un'icona o un'immagine bitmap, accName e accKeyboardShortcut vengono specificati nel campo della guida del record della [tabella di controllo](control-table.md) , a sinistra del \| separatore.
-   Evitare l'uso di controlli di testo su bitmap bianche perché, in Contrasto elevato nero, il testo potrebbe diventare invisibile.
-   Non inserire un controllo di testo nero su uno sfondo costituito da un'immagine bitmap bianca. Questo testo non è visibile a un utente che modifica la visualizzazione di Windows per Contrasto elevato nero.
-   Non inserire un controllo di testo bianco su uno sfondo costituito da un'immagine bitmap nera. Questo testo non è visibile a un utente che modifica la visualizzazione di Windows in Contrasto elevato bianco.
-   Non posizionare [controlli testo](text-control.md) trasparenti su bitmap colorate. Il testo potrebbe non essere visibile se l'utente modifica la combinazione di colori di visualizzazione. Ad esempio, il testo potrebbe diventare invisibile se l'utente imposta il parametro a contrasto elevato per l'accessibilità.
-   Si noti che lo stato attivo su una finestra di dialogo non esegue la tabulazione in un [controllo RadioButtonGroup](radiobuttongroup-control.md) fino a quando non viene selezionato uno dei pulsanti del gruppo. Per impostare la scheda stato attivo su questo gruppo di pulsanti, specificare uno dei pulsanti come impostazione predefinita per il controllo.
-   Per fornire ai programmi di lettura schermo un testo descrittivo aggiuntivo su un [controllo RadioButtonGroup](radiobuttongroup-control.md). Seguire l'esempio fornito in [aggiunta di testo aggiuntivo ai pulsanti di opzione](adding-extra-text-to-radio-buttons.md).
-   La dimensione relativa delle finestre di dialogo, dei controlli e dei tipi di carattere può variare a seconda della dimensione del carattere scelta. Per ulteriori informazioni, vedere [unità del programma di installazione](installer-units.md). Per garantire la visualizzazione corretta del testo e dei controlli nell'interfaccia utente, gli sviluppatori devono sempre testare l'applicazione utilizzando tutte le dimensioni del carattere che potrebbero essere utilizzate.

 

 



