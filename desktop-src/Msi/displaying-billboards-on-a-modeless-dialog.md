---
description: I recinti possono visualizzare una sequenza di immagini e testo in una finestra di dialogo durante un'installazione. In genere, gli elementi vengono usati per creare l'effetto visivo di una presentazione o di un'animazione che informa l'utente dello stato di avanzamento di un'installazione.
ms.assetid: 6432ee7d-0da2-48be-b14c-d36a83a3bb1d
title: Visualizzazione di finestre in una finestra di dialogo non modali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badf81e2b6d0131d1224f10b19e8de3c06f173ef91e3b08f3a45f31aef52be11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086171"
---
# <a name="displaying-billboards-on-a-modeless-dialog"></a>Visualizzazione di finestre in una finestra di dialogo non modali

I recinti possono visualizzare una sequenza di immagini e testo in una finestra di dialogo durante un'installazione. In genere, gli elementi vengono usati per creare l'effetto visivo di una presentazione o di un'animazione che informa l'utente dello stato di avanzamento di un'installazione.

**Per visualizzare i pannelli in una finestra di dialogo non modali**

1.  Includere un record nella tabella [delle finestre di dialogo](dialog-table.md) per la finestra di dialogo non modabile che contiene il tavolo. Dopo la visualizzazione di un pannello, una finestra di dialogo non modabile restituisce il controllo al programma di installazione. In questo modo il programma di installazione può elaborare i messaggi e aggiornare la finestra di dialogo e la finestra di dialogo. Per creare una finestra di dialogo non modale, non impostare il bit di stile della finestra di dialogo modale nel campo Attributi della [tabella delle finestre di dialogo.](dialog-table.md) Il record [tabella finestra di dialogo](dialog-table.md) seguente specifica la finestra di dialogo ActionDialog.

    [Tabella delle finestre di](dialog-table.md) dialogo (parziale)

    | Finestra di dialogo\_     | HCentering | VCentering | Larghezza | Altezza | Attributi | Titolo  | Control \_ First | Impostazione \_ predefinita del controllo | Annullamento \_ del controllo |
    |--------------|------------|------------|-------|--------|------------|--------|----------------|------------------|-----------------|
    | Finestra di dialogo Azione | 50         | 50         | 480   | 240    | 5          | Azione | Annulla         | Annulla           | Annulla          |

    

     

2.  Aggiungere un record alla tabella [di controllo per](control-table.md) specificare che nella finestra di dialogo viene visualizzato un oggetto . Il record definisce le dimensioni e la posizione dell'area nella finestra di dialogo in cui devono essere visualizzati i controlli del controllo elencati nella tabella [BBControl.](bbcontrol-table.md) Il record [Tabella di controllo](control-table.md) seguente definisce la posizione e le dimensioni del pannello nella finestra di dialogo ActionDialog.

    [Tabella di controllo](control-table.md) (parziale)

    | Finestra di dialogo\_     | Control   | Tipo      | X   | S   | Larghezza | Altezza | Attributi |
    |--------------|-----------|-----------|-----|-----|-------|--------|------------|
    | Finestra di dialogo Azione | Billboard | Billboard | 0   | 110 | 480   | 130    | 1          |

    

     

3.  La [tabella dei listini](billboard-table.md) elenca i controlli e specifica quando viene visualizzato un controllo specifico. Aggiungere un record alla tabella [dei pannelli di controllo](billboard-table.md) per ogni controllo. La [tabella di controllo controlla](billboard-table.md) i messaggi di stato inviati durante un'installazione. Un pannello viene visualizzato solo quando un messaggio di stato viene inviato dalle azioni elencate nella colonna Azione della tabella [Dei](billboard-table.md)campi e solo se la funzionalità nel campo Funzionalità è selezionata per \_ l'installazione. Dopo essere stato visualizzato, un'immagine rimane visibile fino a quando non viene coperta da un'altra finestra di dialogo o fino a quando la finestra di dialogo non viene chiusa. Se per un'azione vengono specificati più elementi, questi vengono visualizzati uno alla volta nell'ordine specificato dal campo Ordinamento. Ad esempio, le voci seguenti della tabella [Deifile](billboard-table.md) visualizzano prima i controlli BB1 e BB2 [Quando](billboard-control.md) viene eseguita l'azione [InstallFiles](installfiles-action.md) e la funzionalità QuickTest è stata selezionata per l'installazione.

    [Tabella table (parziale)](billboard-table.md)

    | Billboard | Funzionalità   | Azione       | Ordering |
    |-----------|-----------|--------------|----------|
    | BB1       | Quicktest | InstallFiles | 1        |
    | BB2       | Quicktest | InstallFiles | 2        |

    

     

4.  La [tabella BBControl](bbcontrol-table.md) specifica i controlli che appartengono ai [controlli Controls](billboard-control.md) di Controls elencati nella tabella [Dei BBControl.](billboard-table.md) Il [controllo Text,](text-control.md) [il controllo Bitmap](bitmap-control.md)e il controllo [Icon](icon-control.md) sono gli unici tipi di controlli che possono essere utilizzati. È possibile inserire più controlli in ogni elemento. Immettere il nome del campiello nel campo Dei campi della \_ [tabella BBControl](bbcontrol-table.md) esattamente come appare nella [tabella dei campi.](billboard-table.md)

    Ogni posizione del controllo viene specificata come coordinate dell'angolo superiore sinistro del controllo. L'origine del sistema di coordinate si trova nell'angolo superiore sinistro del controllo del pannello anziché in un angolo della finestra di dialogo. Le coordinate sono in unità di installazione, non in unità di dialogo. Un'unità del programma di installazione è uguale a un dodicesimo dell'altezza delle dimensioni del carattere MS Sans Serif a 10 punti. La tabella [BBControl seguente consente](bbcontrol-table.md) di aggiungere controlli ai controlli .

    [Tabella BBControl](bbcontrol-table.md) (parziale)

    | Billboard | BBControl | Tipo   | X   | S   | Larghezza | Altezza | Attributi | Testo             |
    |-----------|-----------|--------|-----|-----|-------|--------|------------|------------------|
    | BB1       | Testo      | Testo   | 100 | 30  | 280   | 280    | 3          | Primo manifesto  |
    | BB1       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Software         |
    | BB1       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Musica            |
    | BB2       | Testo      | Testo   | 100 | 30  | 280   | 20     | 3          | Secondo tabellone pubblicitario |
    | BB2       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Musica            |
    | BB2       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Software         |

    

     

5.  Per visualizzare un manifesto pubblicitario nella finestra di dialogo ActionDialog, è necessario sottoscrivere il controllo a [SetProgress ControlEvent](setprogress-controlevent.md) aggiungendo un record alla [tabella EventMapping](eventmapping-table.md). Quando il programma di installazione pubblica l'oggetto SetProgress ControlEvent specificato nella colonna Event, il programma di installazione imposta l'attributo del controllo specificato nel campo Attributo. Il campo Event contiene l'identificatore di stringa (senza virgolette) di SetProgress ControlEvent. Il campo Attributo contiene l'identificatore di stringa (senza virgolette) dell'attributo da impostare. I campi Dialogo \_ e \_ Controllo identificano il controllo e devono corrispondere a tali campi nella [tabella di controllo](control-table.md). Ad esempio, la tabella [EventMapping seguente](eventmapping-table.md) sottoscrive un controllo a un evento .

    [Tabella EventMapping](eventmapping-table.md) (parziale)

    | Finestra di dialogo\_     | controllo\_ | Event       | Attributo |
    |--------------|-----------|-------------|-----------|
    | ActionDialog | Billboard | SetProgress | Avanzamento  |

    

     

 

 



