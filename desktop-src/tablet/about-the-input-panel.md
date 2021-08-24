---
description: A partire da Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) versione 1.0, il Pannello input tablet PC a livello di sistema offre un meccanismo universale per eseguire l'input di testo nella piattaforma Windows, anche se non fornisce l'accesso a livello di codice. L'oggetto PenInputPanel di Tablet PC SDK versione 1.5 integra gli strumenti di input di testo nelle applicazioni.
ms.assetid: 14fe4963-ab9b-4c78-9f17-791c68378ef0
title: Informazioni sul Pannello input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044e8c3a43127bd765fd5004329352956e4be8bb9f214f8dda8896fa318832a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844411"
---
# <a name="about-the-input-panel"></a>Informazioni sul Pannello input penna

\[[**PenInputPanel**](peninputpanel-class.md) è stato sostituito da [**TextInput**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel). Per altre informazioni, vedere [Programmazione del pannello input di testo](programming-the-text-input-panel.md).\]

A partire da Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) versione 1.0, il Pannello input tablet PC a livello di sistema offre un meccanismo universale per eseguire l'input di testo nella piattaforma Windows, anche se non fornisce l'accesso a livello di codice. L'oggetto [**PenInputPanel**](peninputpanel-class.md) di Tablet PC SDK versione 1.5 integra gli strumenti di input di testo nelle applicazioni.

Il grafico seguente mostra il pannello di input penna visualizzato [nell'esempio di modulo di attestazioni](auto-claims-form-sample.md) automatico.

![Esempio di pannello di input penna visualizzato sull'esempio di modulo di attestazioni automatico](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

[**L'oggetto PenInputPanel**](peninputpanel-class.md) è utile per gli sviluppatori di applicazioni. Non è necessario sostituire i controlli nei moduli esistenti. È sufficiente associare **oggetti PenInputPanel** ai controlli esistenti che ricevono l'input di testo e possono iniziare a ricevere input dall'oggetto **PenInputPanel.**

[**L'oggetto PenInputPanel**](peninputpanel-class.md) adotta le impostazioni del Pannello di input per le proprietà seguenti:

-   Layout
-   Spessore input penna
-   Timeout di riconoscimento
-   Dimensioni della casella, modalità di invio e altre impostazioni specifiche per l'input boxed dell'Asia orientale

[**L'oggetto PenInputPanel**](peninputpanel-class.md) non fornisce l'accesso all'input penna sottostante. Per ottenere l'input penna, usare il [controllo InkPicture.](inkpicture-control-reference.md)

[**L'oggetto PenInputPanel**](peninputpanel-class.md) fornisce un'interfaccia utente sul posto facilmente individuabile dagli utenti finali delle applicazioni. Viene attivato automaticamente quando l'utente tocca una finestra con un **oggetto PenInputPanel** usando la penna del tablet. Il pannello di input penna viene visualizzato automaticamente quando il sistema rileva un evento CursorButtonUp per la finestra a cui è collegato l'oggetto **PenInputPanel.** L'attivazione automatica può essere disabilitata impostando la [**proprietà AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) su **FALSE.**

Il pannello di input penna non viene visualizzato automaticamente sugli eventi del mouse. Gli eventi penna vengono convertiti in eventi del mouse quando si usano Servizi terminal. [**L'oggetto PenInputPanel**](peninputpanel-class.md) non funziona su una connessione di Servizi terminal.

## <a name="pen-input-panel-input-modes"></a>Modalità di input del pannello input penna

[**L'oggetto PenInputPanel**](peninputpanel-class.md) consente la funzionalità della tastiera o l'input per la scrittura a mano, con tasti di scelta rapida aggiuntivi per facilitare l'input. L'interfaccia utente per il pannello di input penna include:

-   Blocco scrittura
-   Blocco di scrittura per le lingue dell'Asia orientale
-   Tasti rapidi Tasti di scelta rapida
-   Tastiera sul posto

La disponibilità del writing pad rispetto al blocco di scrittura per le lingue dell'Asia orientale dipende dalle impostazioni locali predefinite dell'utente nel sistema operativo.

### <a name="writing-pad"></a>Writing Pad

Il riquadro di scrittura è simile alla nota interfaccia utente del pannello di input.

Il blocco di scrittura raccoglie la grafia dall'utente finale. L'interfaccia utente di base include una singola riga di scrittura in cui l'utente può scrivere testo con una penna digitale. Quando l'utente termina la scrittura e tocca il pulsante Invia o attende che si verifichi un timeout, la grafia viene inviata al sistema di riconoscimento.

L'input penna viene riconosciuto dopo che è trascorso un periodo di tempo specificato dal momento in cui è stato raccolto l'ultimo tratto input penna. Quando si verifica il timeout, l'input penna viene rimosso dalla superficie di raccolta e viene eseguito il riconoscimento. Il testo riconosciuto viene quindi inserito nel controllo a cui è collegato l'oggetto [**PenInputPanel.**](peninputpanel-class.md)

### <a name="east-asian-multibox-pad"></a>Riquadro a più caselle dell'Asia orientale

La versione dell'Asia orientale del pannello di input penna visualizza un'interfaccia a più caselle per l'immissione di caratteri asiatici. Fornisce alternative ed è simile all'interfaccia utente del pannello di input. Gli utenti possono correggere i caratteri non riconosciuti toccando una casella di scrittura e selezionando il carattere corretto da un elenco di alternative nella barra nella parte superiore del pannello di input penna. I pulsanti di filtro sono disponibili per restringere l'elenco di alternative di riconoscimento ai tipi di caratteri specificati, ad esempio i simboli.

Le versioni coreane e giapponesi del pad di scrittura hanno una chiave di conversione oltre ai mini tasti rapidi comuni a tutte le skin linguistiche.

Per ottenere caratteri latini nel blocco di scrittura per le lingue dell'Asia orientale, impostare la proprietà [**Factoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid) per aumentare l'accuratezza del riconoscimento dei caratteri latini. Impostare il **membro Digit** dell'oggetto [**Factoid**](factoid-constants.md) per i caratteri numerici o il membro **OneChar** dell'oggetto **Factoid** per i caratteri alfabetici e numerici.

### <a name="quickkeys-keypads"></a>Tasti di scelta rapida Tasti di scelta rapida

Il pannello di input penna fornisce due tastiere di piccole dimensioni per l'immissione di simboli e numeri.

### <a name="in-place-keyboard"></a>Tastiera sul posto

Il pannello di input penna offre una modalità tastiera per le situazioni in cui il riconoscimento della grafia non è sufficiente. Ad esempio, quando si immette una password o un numero di parte, è probabile che gli utenti oserino più successo usando la tastiera del pannello di input penna rispetto al riquadro di scrittura. Ciò è dovuto al fatto che è improbabile che le password o i numeri di parte siano presenti nel dizionario di riconoscimento del tastierino di scrittura.

## <a name="recognizer-support"></a>Supporto di Recognizer

[**L'oggetto PenInputPanel**](peninputpanel-class.md) supporta i riconoscitori di spedizione Windows XP Tablet PC Edition versione 1.0 e Tablet PC SDK versione 1.5.

## <a name="automatic-positioning"></a>Posizionamento automatico

Per impostazione predefinita, il pannello di input penna viene posizionato automaticamente rispetto al controllo a cui è collegato. Non si sovrappone al controllo a meno che non vi sia spazio sufficiente sullo schermo sia per il pannello di input penna che per il controllo o a meno che lo sviluppatore non imposta in modo esplicito la posizione del pannello di input penna.

Il posizionamento automatico funziona solo quando lo sviluppatore non ha impostato in modo esplicito la posizione usando [**il metodo MoveTo.**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) Per eseguire l'override del posizionamento automatico, modificare i valori delle [**proprietà Top**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) e [**Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) in un [**gestore dell'evento PanelMoving.**](peninputpanel-panelmoving.md)

La posizione del pannello di input penna è vincolata dai bordi dello schermo. Nessun bordo del pannello di input penna può essere più vicino a 0,25 pollici da qualsiasi bordo dello schermo.

Per impostazione predefinita, la parte superiore del pannello di input penna viene visualizzata nella parte inferiore del controllo a cui è associato ed è separata dal controllo dal valore della [**proprietà VerticalOffset.**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset) Se non c'è spazio sufficiente sotto il controllo, la parte inferiore del pannello di input penna viene visualizzata nella parte superiore del controllo a cui è collegato ed è separata dal controllo dal valore della **proprietà VerticalOffset.** Se non è ancora disponibile spazio sufficiente, come nel caso di un controllo di modifica a schermo intero, il pannello di input penna si sovrappone al controllo.

Il pannello di input della penna del bordo sinistro viene visualizzato sul bordo sinistro del controllo a cui è collegato ed è separato dal controllo dal valore della [**proprietà HorizontalOffset,**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset) ad eccezione del limite dello schermo. Se la posizione desiderata posiziona il pannello di input penna oltre i limiti dello schermo disponibili, il pannello di input della penna presuppone la posizione orizzontale più vicina possibile.

### <a name="forced-overlap"></a>Sovrapposizione forzata

A volte è necessario che il pannello di input penna si sovrapponga al controllo associato, come nel caso di un controllo di modifica a schermo intero. In questi casi, il posizionamento automatico del pannello di input penna viene determinato usando le regole seguenti:

-   Quando il punto di inserimento si trova nella metà superiore del controllo associato, la posizione verticale del pannello di input penna si trova nella parte inferiore dello schermo, possibilmente posizionandolo sulla parte inferiore del controllo.
-   Quando il punto di inserimento si trova nella metà inferiore del controllo associato, la posizione verticale del pannello di input penna si trova nella parte superiore dello schermo, possibilmente posizionandolo sopra la metà superiore del controllo.

### <a name="windowless-controls"></a>Controlli senza finestra

Nel caso in cui un [**oggetto PenInputPanel**](peninputpanel-class.md) sia associato a un controllo senza finestra, il pannello di input penna viene posizionato rispetto all'elemento padre del controllo senza finestra. Impostare le [**proprietà Top**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) [**e Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) in un gestore dell'evento [**PanelMoving**](peninputpanel-panelmoving.md) o usare il [**metodo MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) per posizionare manualmente il pannello di input della penna.

 

 
