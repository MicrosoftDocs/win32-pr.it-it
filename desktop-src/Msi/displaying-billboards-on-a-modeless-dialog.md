---
description: I tabelloni possono visualizzare una sequenza di immagini e testo in una finestra di dialogo durante un'installazione. In genere, i tabelloni vengono utilizzati per creare l'effetto visivo di una presentazione o un'animazione che informa l'utente dello stato di avanzamento di un'installazione.
ms.assetid: 6432ee7d-0da2-48be-b14c-d36a83a3bb1d
title: Visualizzazione di manifesti in una finestra di dialogo non modale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fd0ca40e47a8d52c16db7adde304177d4dc849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130690"
---
# <a name="displaying-billboards-on-a-modeless-dialog"></a>Visualizzazione di manifesti in una finestra di dialogo non modale

I tabelloni possono visualizzare una sequenza di immagini e testo in una finestra di dialogo durante un'installazione. In genere, i tabelloni vengono utilizzati per creare l'effetto visivo di una presentazione o un'animazione che informa l'utente dello stato di avanzamento di un'installazione.

**Per visualizzare i tabelloni in una finestra di dialogo non modale**

1.  Includere un record nella [tabella della finestra](dialog-table.md) di dialogo per la finestra di dialogo non modale che contiene il tabellone. Dopo la visualizzazione di un cartello, una finestra di dialogo non modale restituisce il controllo al programma di installazione. Ciò consente al programma di installazione di elaborare i messaggi e aggiornare la finestra di dialogo e il tabellone. Per creare una finestra di dialogo non modale, non impostare il bit di stile della finestra di dialogo modale nel campo attributi della [tabella della finestra di dialogo](dialog-table.md). Il record della [tabella della finestra di dialogo](dialog-table.md) seguente specifica la finestra di dialogo ActionDialog.

    [Tabella finestra di dialogo](dialog-table.md) (parziale)

    | Finestra di dialogo\_     | HCentering | VCenter | Larghezza | Altezza | Attributi | Titolo  | \_Primo controllo | Controllo \_ predefinito | \_Annulla controllo |
    |--------------|------------|------------|-------|--------|------------|--------|----------------|------------------|-----------------|
    | ActionDialog | 50         | 50         | 480   | 240    | 5          | Azione | Annulla         | Annulla           | Annulla          |

    

     

2.  Aggiungere un record alla [tabella dei controlli](control-table.md) per specificare che nella finestra di dialogo viene visualizzato un tabellone. Il record definisce le dimensioni e la posizione dell'area nella finestra di dialogo in cui devono essere visualizzati i controlli del Billboard elencati nella [tabella BBControl](bbcontrol-table.md) . Il record della [tabella di controllo](control-table.md) seguente definisce la posizione e le dimensioni del cartellone nella finestra di dialogo ActionDialog.

    [Tabella di controllo](control-table.md) (parziale)

    | Finestra di dialogo\_     | Control   | Tipo      | X   | S   | Larghezza | Altezza | Attributi |
    |--------------|-----------|-----------|-----|-----|-------|--------|------------|
    | ActionDialog | Billboard | Billboard | 0   | 110 | 480   | 130    | 1          |

    

     

3.  Nella [tabella Billboard](billboard-table.md) sono elencati i controlli Billboard e viene specificato quando viene visualizzato un controllo Billboard specifico. Aggiungere un record alla [tabella Billboard](billboard-table.md) per ogni controllo Billboard. La [tabella Billboard](billboard-table.md) controlla i messaggi di stato inviati durante un'installazione. Un tabellone viene visualizzato solo quando un messaggio di stato viene inviato dalle azioni elencate nella colonna azione della [tabella Billboard](billboard-table.md)e solo se la funzionalità nel \_ campo funzionalità è selezionata per l'installazione. Una volta visualizzato, il tabellone rimane visibile fino a quando non viene coperto da un altro cartello o finché la finestra di dialogo non viene chiusa. Se per un'azione vengono specificati più tabelloni, questi vengono visualizzati uno alla volta nell'ordine specificato dal campo di ordinamento. Ad esempio, le voci della [tabella Billboard](billboard-table.md) seguenti visualizzano prima di tutto il BB1 e quindi il BB2 [Billboard controlla](billboard-control.md) quando viene eseguita l'azione [InstallFiles](installfiles-action.md) e la funzionalità QuickTest è stata selezionata per l'installazione.

    [Tabella Billboard](billboard-table.md) (parziale)

    | Billboard | Funzionalità   | Azione       | Ordering |
    |-----------|-----------|--------------|----------|
    | BB1       | QuickTest | InstallFiles | 1        |
    | BB2       | QuickTest | InstallFiles | 2        |

    

     

4.  La [tabella BBControl](bbcontrol-table.md) specifica i controlli che appartengono ai [controlli Billboard](billboard-control.md) elencati nella [tabella Billboard](billboard-table.md). Il controllo [testo](text-control.md), il [controllo bitmap](bitmap-control.md)e il [controllo icona](icon-control.md) sono gli unici tipi di controlli che possono essere inseriti in un tabellone. In ogni Billboard è possibile inserire più controlli. Immettere il nome del Billboard nel \_ campo Billboard della [tabella BBControl](bbcontrol-table.md) esattamente come appare nella [tabella Billboard](billboard-table.md).

    Ogni posizione del controllo viene specificata come coordinate dell'angolo superiore sinistro del controllo. L'origine del sistema di coordinate si trova nell'angolo superiore sinistro del controllo Billboard anziché in un angolo della finestra di dialogo. Le coordinate si trovano nelle unità del programma di installazione, non nelle unità di dialogo. Un'unità del programma di installazione è uguale a un dodicesimo dell'altezza delle dimensioni del carattere MS Sans Serif a 10 punti. La [tabella BBControl](bbcontrol-table.md) seguente registra i controlli per i tabelloni.

    [Tabella BBControl](bbcontrol-table.md) (parziale)

    | Billboard | BBControl | Tipo   | X   | S   | Larghezza | Altezza | Attributi | Testo             |
    |-----------|-----------|--------|-----|-----|-------|--------|------------|------------------|
    | BB1       | Testo      | Testo   | 100 | 30  | 280   | 280    | 3          | Primo cartellone  |
    | BB1       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Software         |
    | BB1       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Musica            |
    | BB2       | Testo      | Testo   | 100 | 30  | 280   | 20     | 3          | Secondo tabellone |
    | BB2       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Musica            |
    | BB2       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Software         |

    

     

5.  Per visualizzare un tabellone nella finestra di dialogo ActionDialog, è necessario sottoscrivere il controllo Billboard per l' [esecuzione di ControlEvent](setprogress-controlevent.md) mediante l'aggiunta di un record alla [tabella EventMapping](eventmapping-table.md). Quando il programma di installazione pubblica il ControlEvent di avanzamento specificato nella colonna evento, il programma di installazione imposta l'attributo del controllo specificato nel campo attributo. Il campo evento contiene l'identificatore di stringa (senza virgolette) del ControlEvent di avanzamento. Il campo attributo contiene l'identificatore di stringa (senza virgolette) dell'attributo da impostare. I campi della finestra di dialogo \_ e del controllo \_ identificano il controllo Billboard e devono corrispondere a tali campi nella [tabella dei controlli](control-table.md). La [tabella EventMapping](eventmapping-table.md) seguente, ad esempio, sottoscrive un controllo a un evento.

    [Tabella EventMapping](eventmapping-table.md) (parziale)

    | Finestra di dialogo\_     | controllo\_ | Evento       | Attributo |
    |--------------|-----------|-------------|-----------|
    | ActionDialog | Billboard | SetProgress | Avanzamento  |

    

     

 

 



