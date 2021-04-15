---
description: A partire da Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) versione 1,0, il pannello di input di Tablet PC a livello di sistema fornisce un meccanismo universale per eseguire l'input di testo nella piattaforma Windows, anche se non fornisce l'accesso a livello di codice. L'oggetto PenInputPanel di Tablet PC SDK versione 1,5 integra gli strumenti di input di testo nelle applicazioni.
ms.assetid: 14fe4963-ab9b-4c78-9f17-791c68378ef0
title: Informazioni sul pannello input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7db733e49e49d428b5ff8072a1315787d9fafd25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401521"
---
# <a name="about-the-input-panel"></a>Informazioni sul pannello input

\[[**PenInputPanel**](peninputpanel-class.md) è stato sostituito da [**TextInput**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel). Per altre informazioni, vedere [Programming the text input panel](programming-the-text-input-panel.md).\]

A partire da Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) versione 1,0, il pannello di input di Tablet PC a livello di sistema fornisce un meccanismo universale per eseguire l'input di testo nella piattaforma Windows, anche se non fornisce l'accesso a livello di codice. L'oggetto [**PenInputPanel**](peninputpanel-class.md) di Tablet PC SDK versione 1,5 integra gli strumenti di input di testo nelle applicazioni.

Il grafico seguente mostra il pannello input penna visualizzato nell'esempio di [esempio di modulo delle attestazioni automatiche](auto-claims-form-sample.md) .

![Pannello input penna visualizzato sull'esempio di esempio di modulo delle attestazioni automatico](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

L'oggetto [**PenInputPanel**](peninputpanel-class.md) è utile per gli sviluppatori di applicazioni. Non è necessario sostituire i controlli nei moduli esistenti. È sufficiente alleghi gli oggetti **PenInputPanel** ai controlli esistenti che ricevono input di testo e possono iniziare a ricevere input dall'oggetto **PenInputPanel** .

L'oggetto [**PenInputPanel**](peninputpanel-class.md) adotta le impostazioni del pannello di input per le proprietà seguenti:

-   Layout
-   Spessore input penna
-   Timeout riconoscimento
-   Dimensioni box, modalità di invio e altre impostazioni specifiche per l'input boxed dell'Asia orientale

L'oggetto [**PenInputPanel**](peninputpanel-class.md) non fornisce l'accesso all'input penna sottostante. Per ottenere l'input penna, utilizzare il controllo [InkPicture](inkpicture-control-reference.md) .

L'oggetto [**PenInputPanel**](peninputpanel-class.md) fornisce un'interfaccia utente (UI) sul posto facilmente individuabile dagli utenti finali delle applicazioni. Viene attivato automaticamente quando l'utente tocca una finestra con un oggetto **PenInputPanel** usando la penna del tablet. Il pannello input penna viene visualizzato automaticamente quando il sistema rileva un evento CursorButtonUp per la finestra a cui è associato l'oggetto **PenInputPanel** . L'attivazione automatica può essere disabilitata impostando la proprietà [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) su **false**.

Il pannello input penna non viene visualizzato automaticamente negli eventi del mouse. Gli eventi penna vengono convertiti in eventi del mouse quando si utilizza Servizi terminal. L'oggetto [**PenInputPanel**](peninputpanel-class.md) non funziona su una connessione Servizi terminal.

## <a name="pen-input-panel-input-modes"></a>Modalità di input del pannello input penna

L'oggetto [**PenInputPanel**](peninputpanel-class.md) consente la funzionalità della tastiera o l'input della grafia, con tasti di scelta rapida aggiuntivi per supportare l'input. L'interfaccia utente per il pannello input penna include:

-   Creazione di un riquadro
-   Riquadro di scrittura per le lingue asiatiche orientali
-   Tasti di QuickKeys
-   Tastiera sul posto

La disponibilità del riquadro di scrittura rispetto al riquadro di scrittura per le lingue asiatiche orientali dipende dalle impostazioni locali predefinite dell'utente nel sistema operativo.

### <a name="writing-pad"></a>Creazione di un riquadro

Il riquadro di scrittura è simile alla nota interfaccia utente del pannello di input.

Il riquadro di scrittura raccoglie la grafia dall'utente finale. L'interfaccia utente di base include una singola riga di scrittura in cui l'utente può scrivere testo con una penna digitale. Quando l'utente termina la scrittura e tocca il pulsante Invia o attende il verificarsi di un timeout, viene inviata una grafia al riconoscimento.

L'input penna viene riconosciuto dopo che è trascorso un periodo di tempo specificato dal momento in cui è stato raccolto l'ultimo tratto di input penna. Quando si verifica il timeout, l'input penna viene rimosso dalla superficie della raccolta e si verifica il riconoscimento. Il testo riconosciuto viene quindi inserito nel controllo a cui è associato l'oggetto [**PenInputPanel**](peninputpanel-class.md) .

### <a name="east-asian-multibox-pad"></a>Riquadro MultiBox asiatico orientale

La versione Asia orientale del pannello input penna Visualizza un'interfaccia MultiBox per l'immissione di caratteri asiatici. Fornisce alternative ed è simile all'interfaccia utente del pannello di input. Gli utenti possono correggere i caratteri non riconosciuti toccando una casella di scrittura e selezionando il carattere corretto da un elenco di alternative nella barra nella parte superiore del pannello input penna. Sono disponibili pulsanti filtro per limitare l'elenco delle alternative di riconoscimento ai tipi di caratteri specificati, ad esempio i simboli.

Le versioni coreano e giapponese del riquadro di scrittura dispongono di una chiave di conversione oltre alle mini rapide chiavi comuni a tutte le interfacce della lingua.

Per ottenere caratteri latini nel riquadro di scrittura per le lingue asiatiche orientali, impostare [**la proprietà del**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid) controllo del controllo per aumentare l'accuratezza del riconoscimento dei caratteri latini. Impostare il **membro digit** [**dell'oggetto del**](factoid-constants.md) controllore per i caratteri numerici o il membro **OneChar** dell'oggetto del controllore **per i caratteri** alfabetici e numerici.

### <a name="quickkeys-keypads"></a>Tasti di QuickKeys

Il pannello input penna fornisce due piccoli tasti di tastiera per l'immissione di simboli e numeri.

### <a name="in-place-keyboard"></a>Tastiera sul posto

Il pannello input penna fornisce una modalità tastiera per le situazioni in cui il riconoscimento della grafia non è sufficiente. Ad esempio, quando si immette una password o un numero di parte, è probabile che gli utenti abbiano più successo usando la tastiera del pannello input penna rispetto al riquadro di scrittura. Questo è dovuto al fatto che è improbabile che le password o i numeri di parte siano presenti nel dizionario di riconoscimento del riquadro di scrittura.

## <a name="recognizer-support"></a>Supporto del riconoscimento

L'oggetto [**PenInputPanel**](peninputpanel-class.md) supporta la distribuzione di riconoscitori per Windows XP Tablet PC Edition versione 1,0 e Tablet PC SDK versione 1,5.

## <a name="automatic-positioning"></a>Posizionamento automatico

Per impostazione predefinita, il pannello input penna viene posizionato automaticamente in relazione al controllo a cui è collegato. Non si sovrappone al controllo, a meno che non vi sia una sufficiente proprietà dello schermo per il pannello input penna e il controllo oppure, a meno che lo sviluppatore non imposti esplicitamente la posizione del pannello input penna.

Il posizionamento automatico funziona solo quando lo sviluppatore non ha impostato in modo esplicito la posizione utilizzando il metodo [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) . Per eseguire l'override del posizionamento automatico, modificare i valori delle proprietà [**Top**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) e [**Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) in un gestore eventi [**PanelMoving**](peninputpanel-panelmoving.md) .

La posizione del pannello input penna è vincolata dai bordi dello schermo. Nessun bordo del pannello input penna può essere più vicino a 0,25 centimetri da qualsiasi bordo dello schermo.

Per impostazione predefinita, la parte superiore del pannello input penna viene visualizzata nella parte inferiore del controllo a cui è collegata ed è separata dal controllo in base al valore della proprietà [**VerticalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset) . Se non è disponibile spazio sufficiente sotto il controllo, la parte inferiore del pannello input penna viene visualizzata nella parte superiore del controllo a cui è collegata ed è separata dal controllo in base al valore della proprietà **VerticalOffset** . Se non è ancora disponibile spazio sufficiente, come nel caso di un controllo di modifica a schermo intero, il pannello input penna si sovrappone al controllo.

Il pannello input penna del bordo sinistro viene visualizzato al bordo sinistro del controllo a cui è collegato ed è separato dal controllo in base al valore della proprietà [**HorizontalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset) , fatta eccezione per la delimitazione dello schermo. Se la posizione desiderata posiziona il pannello input penna oltre i limiti di schermo disponibili, il pannello input penna assume la posizione orizzontale più vicina possibile.

### <a name="forced-overlap"></a>Sovrapposizione forzata

A volte è necessario che il pannello input penna si sovrappongano al controllo collegato, come nel caso di un controllo di modifica a schermo intero. In questi casi, il posizionamento automatico del pannello input penna viene determinato in base alle regole seguenti:

-   Quando il punto di inserimento si trova nella metà superiore del controllo collegato, la posizione verticale del pannello input penna si trova nella parte inferiore dello schermo, possibilmente posizionando la parte inferiore del controllo.
-   Quando il punto di inserimento si trova nella metà inferiore del controllo collegato, la posizione verticale del pannello input penna si trova nella parte superiore della schermata, possibilmente inserendola nella metà superiore del controllo.

### <a name="windowless-controls"></a>Controlli senza finestra

Nel caso in cui un oggetto [**PenInputPanel**](peninputpanel-class.md) venga associato a un controllo senza finestra, il pannello input penna è posizionato in relazione all'elemento padre del controllo privo di finestra. Impostare le proprietà [**Top**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) e [**Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) in un gestore eventi [**PanelMoving**](peninputpanel-panelmoving.md) oppure utilizzare il metodo [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) per posizionare manualmente il pannello input penna.

 

 
