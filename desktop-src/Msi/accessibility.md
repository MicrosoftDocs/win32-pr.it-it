---
description: Gli autori devono essere a conoscenza delle tabelle e dei campi nell'elenco seguente quando progettano l'interfaccia utente in modo che sia conforme alle Active Accessibility guida.
ms.assetid: 516e504e-7895-4388-a38e-fd2fc7dfd61d
title: Accessibilità (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8811d47bc7288e966ca5d536b435611c79fd81f3a38fa0b2dbdd422b5939a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078231"
---
# <a name="accessibility-windows-installer"></a>Accessibilità (Windows Installer)

Gli autori devono essere a conoscenza delle tabelle e dei campi nell'elenco seguente quando progettano l'interfaccia utente in modo che sia conforme alle Active Accessibility guida. L'interfaccia utente di un pacchetto del programma di installazione deve facilitare l'accessibilità dell'applicazione o del prodotto a tutti gli utenti.

-   Il testo della descrizione comando è contenuto nella colonna Guida della [tabella Control](control-table.md). Questo testo viene visualizzato dalle utilità per la lettura dello schermo per i controlli contenenti un'immagine.
-   Il campo Text della [tabella Control per](control-table.md) i controlli [VolumeCostList](volumecostlist-control.md), [ListView](listview-control.md), [DirectoryList](directorylist-control.md) e [SelectionTree](selectiontree-control.md) non viene mai visualizzato. Può invece essere letto dalle utilità di revisione dello schermo come descrizione del controllo. Gli utenti che non possono usare le informazioni visive sullo schermo possono interpretare le informazioni con l'aiuto di un'utilità di revisione dello schermo. Le utilità di revisione dello schermo (definite anche programmi di lettura dello schermo o utilità di accesso vocale) prendono le informazioni visualizzate sullo schermo e le indirizzano tramite supporti alternativi, ad esempio voce sintetizzata o uno schermo Braille aggiornabile.
-   I controlli nelle finestre di dialogo devono essere collegati usando il campo Controllo \_ successivo della tabella [Controllo](control-table.md). I controlli devono essere creati in modo che tutti possano essere raggiunti usando il tasto TAB.
-   I tasti di scelta rapida devono essere forniti per ottenere direttamente l'accesso ai controlli.
-   Il colore del testo visualizzato nell'interfaccia utente è impostato nella [tabella TextStyle](textstyle-table.md). Se il colore del testo scelto è troppo vicino a quello dello sfondo, la scelta del colore del testo viene ignorata.
-   Le dimensioni e il tipo di carattere del testo sono impostati nella [tabella TextStyle](textstyle-table.md). È consigliabile usare caratteri di dimensioni maggiori per i pacchetti destinati al mercato asiatico. Ad esempio, una dimensione del carattere di 10 punti leggibile per il testo in inglese potrebbe non essere necessariamente vera per il cinese.
-   Per i controlli [](text-control.md) [Edit](edit-control.md), [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) o [VolumeSelectCombo](volumeselectcombo-control.md), le utilità per la lettura dello schermo accettano accName e accKeyboardShortcut da un controllo di testo che deve precedere il controllo nella sequenza Control Next della finestra di \_ dialogo. L'utilità per la lettura dello schermo accetta accName dal campo Text del controllo Text e accKeyboardShortcut dalla scelta rapida da tastiera nel campo Text, se esiste un collegamento.
-   Poiché il testo statico non può assumere lo stato attivo, un controllo [Text](text-control.md) che descrive un controllo [Edit](edit-control.md), [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) o [VolumeSelectCombo](volumeselectcombo-control.md) deve essere il primo controllo nella finestra di dialogo per garantire la compatibilità con le utilità per la lettura dello schermo.
-   Per un [controllo PushButton](pushbutton-control.md) che visualizza un'icona o un'immagine bitmap, accName e accKeyboardShortcut vengono specificati nel campo Guida del record della tabella [Control,](control-table.md) a sinistra del \| separatore.
-   Evitare l'uso di controlli di testo sulle bitmap di colore bianco perché in Contrasto elevato nero il testo potrebbe diventare invisibile.
-   Non inserire un controllo di testo nero su uno sfondo che è un'immagine bitmap tutta bianca. Questo testo non è visibile a un utente che modifica la visualizzazione Windows in Contrasto elevato Nero.
-   Non inserire un controllo di testo bianco su uno sfondo che è un'immagine bitmap tutta nera. Questo testo non è visibile a un utente che modifica la visualizzazione Windows in Contrasto elevato bianco.
-   Non posizionare i controlli [Text trasparenti](text-control.md) sopra le bitmap colorate. Il testo potrebbe non essere visibile se l'utente modifica la combinazione di colori di visualizzazione. Ad esempio, il testo può diventare invisibile se l'utente imposta il parametro di contrasto elevato per l'accessibilità.
-   Si noti che lo stato attivo di una finestra di dialogo non viene associato a un [controllo RadioButtonGroup](radiobuttongroup-control.md) fino a quando non viene selezionato uno dei pulsanti del gruppo. Per impostare la scheda dello stato attivo su questo gruppo di pulsanti, specificare uno dei pulsanti come impostazione predefinita per il controllo.
-   Per fornire ai programmi di lettura dello schermo testo descrittivo aggiuntivo su [un controllo RadioButtonGroup.](radiobuttongroup-control.md) Seguire l'esempio fornito in [Aggiunta di testo aggiuntivo ai pulsanti di opzione](adding-extra-text-to-radio-buttons.md).
-   Le dimensioni relative di dialoghe, controlli e tipi di carattere possono variare a seconda della dimensione del carattere scelta. Per altre informazioni, vedere [Unità del programma di installazione](installer-units.md). Per garantire la corretta visualizzazione di testo e controlli nell'interfaccia utente, gli sviluppatori di installazione devono sempre testare l'applicazione usando tutte le dimensioni dei caratteri che potrebbero essere usate.

 

 



