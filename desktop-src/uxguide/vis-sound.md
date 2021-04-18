---
title: Suoni
description: Sound è l'elemento audio dell'esperienza utente.
ms.assetid: 2a276370-eff9-4844-b008-eba9ae5ac395
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 664d78d00cf75dae8f43717db07290a26574f0c6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104567425"
---
# <a name="sound"></a>Suoni

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

*Sound* è l'elemento audio dell'esperienza utente. Se usati in modo appropriato, il suono può essere una forma efficace di comunicazione che stabilisce una relazione non verbale e persino emotiva con gli utenti. I suoni possono essere usati singolarmente o come supplemento per l'interfaccia utente visiva. Ad esempio, l'aggiunta di un effetto audio a una notifica aumenta la probabilità che venga rilevata, soprattutto se l'utente non Visualizza lo schermo quando si verifica un evento.

![screenshot della finestra di dialogo audio ](images/vis-sound-image1.png)

Dalla scheda suoni dell'elemento del pannello di controllo audio, gli utenti possono apportare modifiche ai suoni del sistema.

Questo articolo illustra l'uso di suoni all'interno di un programma come risposta a eventi e azioni degli utenti e l'integrazione del controllo audio di un programma con Windows. Non copre l'uso di musica o sintesi vocale.

**Nota:** Le linee guida relative alle [notifiche](mess-notif.md) e alla [personalizzazione](exper-branding.md) sono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere se usare il suono, prendere in considerazione le domande seguenti:

-   **Il vantaggio di un utente è evidente nell'uso di un suono?** Poiché gli svantaggi dell'uso del suono possono superare facilmente i vantaggi, usare il suono solo quando esiste un vantaggio evidente.
-   **L'uso del suono è appropriato?** L'uso di Sound attirare l'attenzione su elementi degni di attenzione? Gli utenti perderanno il suono se fosse assente? Concentrarsi sui suoni che consentono agli utenti di essere informati, probabilmente modificare il comportamento o fornire commenti e suggerimenti utili.
-   **Si tratta dell'utilizzo del suono che distrae?** Sono presenti suoni frequenti, forti e stonati? È probabile che gli utenti riducano il volume di sistema o il volume del programma come risultato dell'utilizzo del suono?
-   **Si sta usando un suono come una forma di comunicazione principale?** In molti casi, ad esempio per gli utenti che hanno un certo livello di perdita uditiva, non è consigliabile usare l'audio come mezzo di comunicazione principale. Il suono è più efficace come supplemento per altre modalità di comunicazione, ad esempio testo o oggetti visivi.
-   **Gli utenti di destinazione primari sono professionisti IT?** Il suono è in genere inefficace per le attività destinate ai professionisti IT perché molte delle attività vengono eseguite in modo automatico. Inoltre, l'audio non viene ridimensionato in modo da immaginare di eseguire centinaia di attività alla volta e ottenere i suoni quando vengono completati o non riescono.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

In genere, il suono raggiunge uno o tutti gli scopi seguenti:

-   **Notifica.** Il suono può essere associato a eventi specifici. Ad esempio, un suono "nuovo messaggio" indica agli utenti quando arriva la posta senza compromettere l'attività corrente.
-   **Feedback.** Il suono può fornire commenti e suggerimenti per azioni utente specifiche. Ad esempio, un suono sottile che riproduce quando si rilascia il dispositivo di scorrimento nel controllo volume fornisce commenti e suggerimenti sul livello dell'impostazione corrente.
-   **Branding.** Il suono può essere associato a contenuti specifici per personalizzare il prodotto, l'applicazione o il servizio. Windows utilizza il suono in questo modo per l'avvio del sistema operativo.
-   **Intrattenimento.** Il suono viene comunemente usato per migliorare i prodotti di intrattenimento e per rendere più accattivante qualsiasi prodotto. Ad esempio, la maggior parte dei giochi, le applicazioni di formazione e i prodotti di consumo utilizzano un suono per intrattenere gli utenti e migliorare l'esperienza.

Determinati suoni possono soddisfare molti di questi scopi in una sola volta. Il suono di avvio di Windows, ad esempio, indica che il processo di avvio è stato completato e che il desktop è pronto per l'utilizzo. Fornisce inoltre una forma potente di personalizzazione dei prodotti e anche momentaneamente coinvolge gli utenti.

I suoni che soddisfano nessuno di questi scopi dovrebbero essere probabilmente eliminati.

### <a name="inappropriate-use-of-sound"></a>Uso non appropriato del suono

**Nonostante i vantaggi del suono, l'uso appropriato del suono richiede una limitazione significativa a tale scopo può comportare un programma fastidioso e distrazione.** Gli utenti spengono completamente il proprio suono se si infastidiscono in modo frequente, ripetitivo, stridente, sconvolgente e progettato male; in parte questo perché, per sua natura, il suono richiede attenzione ed è difficile ignorarlo. Per suggerimenti su come trovare un equilibrio ragionevole, vedere le [linee guida di progettazione valide](#sound-design).

Poiché gli svantaggi dell'uso del suono possono superare facilmente i vantaggi, usare il suono solo quando esiste un vantaggio evidente. **In caso di dubbi, non usare un suono.**

### <a name="make-sound-supplemental"></a>Rendere audio supplementare

Anche se il suono viene usato in modo appropriato, esistono molte situazioni in cui il suono potrebbe non essere efficace per tutti gli utenti:

-   Alcuni utenti possono lavorare in un ambiente rumoroso in cui non è possibile udire i suoni.
-   Alcuni utenti possono funzionare in un ambiente non interattivo che richiede che il suono venga disattivato o impostato su un volume basso.
-   Alcuni utenti potrebbero avere problemi di udito o perdita.
-   Il computer potrebbe non avere altoparlanti.

Per questi motivi, **il suono usato per le notifiche e il feedback non dovrebbe mai essere l'unico metodo di comunicazione,** ma deve aggiungere suggerimenti visivi o testuali.

### <a name="desirable-characteristics-of-sound"></a>Caratteristiche auspicabili del suono

In generale, i suoni devono essere:

-   da mid ad High Frequency (600 Hertz \[ Hz \] a 2 kilohertz \[ kHz \] ).
-   Short (meno di un secondo).
-   soft o moderato nel volume.
-   significativo.
-   piacevole, non allarmante o stonato.
-   non verbale.
-   non ripetitivo.

Con il suono, less è più. **L'effetto acustico ideale è quello che gli utenti si accorgono a malapena, ma che mancano se fosse assente.**

**Un malinteso comune è che i suoni per gli eventi critici devono essere forti e stonati per attirare l'attenzione dell'utente.** Questo non è vero, perché il suono è effettivamente progettato per essere un mezzo di comunicazione supplementare. Nel caso di un messaggio di errore critico, la relativa presentazione (probabilmente in una finestra di dialogo modale), la relativa icona (un'icona di errore) e il testo e il tono vengono combinati per comunicare la natura dell'errore. Un suono di errore effettivo può essere leggermente più rumoroso rispetto al normale suono di Windows, ma non deve essere significativamente più potente.

### <a name="characteristics-of-windows-sounds"></a>Caratteristiche dei suoni di Windows

Al di là di questa chiamata generale per il minimo, l'aspetto estetico di Windows usa i suoni chiaro, puri e vitrei, con una dissolvenza flessibile e una dissolvenza ("bordi") per evitare effetti improvvisi, stridente e a percussione. Sono progettate per essere sottili, delicate e consonanti. I suoni di Windows usano Echo, Reverb e equalation per ottenere un aspetto naturale e ambientale.

Lo schema audio predefinito per Windows non usa in genere suoni strumentali o riconoscibili quotidianamente che sono troppo specifici o musicali. Esempi di suoni evitati sono strumenti musicali, ad esempio pianoforti o percussioni, suoni di animali, rumori ambientali, sintesi vocale, voci, effetti audio di tipo film o altri suoni di persone. Inoltre, i suoni di Windows non sono pensati per essere percepiti come brani musicali (vale a dire melodie più lunghe, più note). In questo modo, i suoni di Windows sono distinti dal punto di vista funzionale da altri tipi di suoni.

Poiché i suoni di Windows sono stati progettati professionalmente per avere le caratteristiche desiderate e si rivolgono a un vasto pubblico, **provare a usare questi suoni predefiniti di Windows quando appropriato.**

### <a name="designing-your-own-sounds"></a>Progettazione di suoni personalizzati

Se è necessario creare suoni personalizzati, progettarli per avere le caratteristiche descritte in precedenza. Si vuole fare in modo che siano complementari alle attività o agli eventi associati.

Si noti che la creazione di suoni originali è molto difficile da fare in particolare per i suoni destinati a un vasto pubblico. Il suono può essere un elemento di progettazione polarizzato. Per ogni utente che ama un suono, saranno presenti molti utenti che non lo amano.

**Progettare i suoni del programma come gruppo in modo che siano varianti correlate in un tema.** L'esperienza uditiva del programma dovrebbe essere coordinata con la relativa esperienza visiva. Inoltre, il "tono" dei suoni deve essere coordinato con il [tono del testo](text-style-tone.md). Si prenda in considerazione il modo in cui il testo con un tono naturale gradevole può essere sottoposto a una forte presenza di suoni allarmanti.

**Se si eseguono solo quattro operazioni...**

1.  Usare un suono con la limitazione assicurarsi che sia presente un vantaggio utente complessivo chiaro. In caso di dubbi, non usare un suono.
2.  Usare i suoni predefiniti di Windows quando appropriato.
3.  Se si progettano suoni personalizzati, assicurarsi che dispongano delle caratteristiche audio desiderate e che si tratti di varianti di un tema.
4.  Non presupporre che i suoni debbano essere forti e stonati per attirare l'attenzione dell'utente.

## <a name="usage-patterns"></a>Modelli di utilizzo

I suoni hanno diversi modelli di utilizzo:



|                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Completamento azione**<br/> notifica in modo sonico agli utenti quando un'azione avviata dall'utente con esecuzione prolungata viene completata correttamente. <br/>                             | ![screenshot della finestra di dialogo di download del file ](images/vis-sound-image2.png)<br/> In questo esempio la finestra di dialogo riproduce un suono per notificare agli utenti che il download è stato completato.<br/>                                                                                                                                                                                                                                      |
| **Errore azione**<br/> Invia una notifica in modo sonico agli utenti quando un'azione avviata dall'utente con esecuzione prolungata ha esito negativo. <br/>                                                 | ![cattura di schermata del messaggio del disco di backup non accessibile ](images/vis-sound-image3.png)<br/> In questo esempio, Windows riproduce un suono per notificare agli utenti che l'operazione di backup non è riuscita.<br/>                                                                                                                                                                                                                                  |
| **Evento di sistema importante**<br/> avvisa in modo sonico gli utenti di importanti eventi di sistema o dello stato che richiedono attenzione immediata. <br/>                      | ![screenshot del messaggio a batteria insufficiente ](images/vis-sound-image4.png)<br/> In questo esempio gli utenti vengono avvisati che la batteria insufficiente richiede attenzione immediata.<br/>                                                                                                                                                                                                                                                      |
| **FYI**<br/> consente di notificare sonicamente agli utenti le informazioni rilevanti e potenzialmente utili. <br/>                                                                 | Poiché queste informazioni in genere non richiedono l'attenzione immediata, un segnale acustico fornisce un feedback sottile senza compromettere il flusso dell'utente. <br/> ![screenshot del messaggio di accesso Live Messenger ](images/vis-sound-image5.png)<br/> In questo esempio, un suono viene riprodotto quando un contatto accede a un servizio di messaggistica istantanea.<br/>                                                                                 |
| **Effetto audio**<br/> fornisce commenti e suggerimenti sulle interazioni degli utenti. <br/>                                                                            | Fornisce un feedback audio reale o con stile appropriato per l'interazione. gli effetti acustici spesso sono validi come se l'utente manipolasse un oggetto fisico reale. noto anche come Foley. <br/> ![screenshot della finestra ridotta a icona ](images/vis-sound-image6.png)<br/> In questo esempio, l'effetto acustico della finestra Riduci a icona sembra che un oggetto reale venga ridotto di dimensioni.<br/> |
| **Suoni di personalizzazione**<br/> un suono fornito per migliorare l'esperienza utente anche se l'impatto emotivo e, come effetto collaterale, promuove il marchio del prodotto. <br/> | I suoni di personalizzazione sono migliori quando vengono sincronizzati con gli eventi visivi, in particolare le transizioni dell'interfaccia utente, ad esempio la visualizzazione di una finestra del programma. i marchi reali indicano l'origine dei beni, in modo analogo a una parola o un logo marchiato, e sono relativamente rari. <br/> ![screenshot dell'icona di avvio di Windows ](images/vis-sound-image7.png)<br/> In questo esempio, l'avvio di Windows è un'esperienza di transizione personalizzata.<br/>      |



 

## <a name="guidelines"></a>Indicazioni

### <a name="usage"></a>Utilizzo

-   **Usare un suono con la limitazione** assicurarsi che sia presente un vantaggio utente complessivo chiaro. Concentrarsi sui suoni che consentono agli utenti di essere informati, probabilmente modificare il comportamento o fornire commenti e suggerimenti utili. In caso di dubbi, non usare un suono.
-   **Selezionare il suono e le relative caratteristiche in base al modo in cui viene usato.** Per una descrizione di ogni modello di utilizzo, vedere la tabella nella sezione precedente.
-   **Per le notifiche e il feedback, non usare il suono come unico metodo di comunicazione.** Usare invece Sound come metodo supplementare per rinforzare i segnali visivi o testuali. In questo modo si garantisce che gli utenti possano visualizzare le informazioni se non riescono a ascoltare il suono.
-   **Non riprodurre spesso suoni forti o rigidi.** Questa operazione non è necessaria e comporta un'esperienza utente insufficiente. Più spesso viene riprodotto un suono, minore è il numero di invasivo. Per attirare l'attenzione, non è necessario che i suoni siano troppo o troppo rigidi.
-   **Non emettere segnali acustici.** Il segnale acustico non è appropriato per i programmi moderni. Ai segnali acustici non può essere assegnato un significato specifico e gli utenti non possono controllarli.
    -   **Eccezione:** Le funzioni di sistema critiche possono emettere un segnale acustico per avvisare gli utenti delle situazioni in cui devono partecipare immediatamente, ad esempio con una batteria a batteria insufficiente.

### <a name="playback"></a>Riproduzione

-   **Non ripetere un suono più di due volte consecutivamente.**
-   **Per una sequenza consecutiva di eventi audio correlati, riprodurre un suono solo sul primo evento.** Evitare di usare più suoni perché potrebbero entrare in collisione tra loro o causare un'esperienza utente spiacevole.

### <a name="sound-selection"></a>Selezione audio

-   **Scegliere suoni piacevoli.** Non usare suoni sgradevoli, allarmanti, ad esempio ronzio, arresti anomali e interruzioni.
-   **Usare suoni brevi** (meno di un secondo).
-   **Utilizzare suoni approssimativamente dello stesso volume del tipico suono di Windows.** Gli utenti non amano dover spegnere il volume quando avviano un computer o un programma, soprattutto in ambienti pubblici come riunioni e presentazioni. I file audio di Microsoft Windows si trovano nella cartella media all'interno della cartella Windows.
-   **Non scegliere suoni per i quali è necessaria la localizzazione.** A tale scopo, è possibile utilizzare suoni che non utilizzano la voce di riconoscimento vocale o con significati o connotazioni dipendenti dalle impostazioni cultura.

### <a name="windows-system-sounds"></a>Suoni del sistema Windows

-   **Usare i suoni del sistema Windows incorporati ogni volta che è appropriato.**
-   **Scegliere di usare i suoni di sistema in base al significato associato, non solo al suono.** I suoni di sistema devono essere usati in modo coerente.

### <a name="sound-design"></a>Progettazione audio

Quando si creano suoni personalizzati:

-   **Creare suoni con le caratteristiche del suono auspicabili.**
-   **Comporre suoni con la maggior parte del mid-range fino a frequenze elevate (da 600 Hz a 2 kHz).** Non usare frequenze basse perché si spostano oltre, sono più difficili da individuare e possono essere allarmanti.
-   **Impostare l'ampiezza relativa dei suoni normali sul livello del suono di Windows tipico.** I suoni di Windows sono stati opportunamente livellati per gli ambienti domestici e lavorativi. L'uso di livelli diversi per i suoni forza gli utenti a apportare modifiche al volume.
    -   Impostare i suoni importanti in modo che siano leggermente più potenti. Tali suoni includono i completamenti delle azioni, gli errori di azione e gli eventi di sistema importanti.
    -   Impostare i suoni che si verificano di frequente in modo che siano leggermente più morbidi. Sono inclusi FYIs, suoni di personalizzazione e effetti audio.
-   **Scegliere suoni coerenti con il significato dei suoni di Windows.** Per creare una versione personalizzata di un suono Windows, mantenere lo stesso passo e intervallo, ma modificare l'orchestrazione o il timbro. Non assegnare significati diversi ai suoni con passi e intervalli simili come suoni di Windows.
-   **Progettare i suoni per il programma in modo che siano varianti correlate in un tema.** L'esperienza uditiva del programma dovrebbe essere coordinata con la relativa esperienza visiva.
    -   **Progetta transizioni di scena e transizioni audio insieme.** Se, ad esempio, una scena si dissolve gradualmente, qualsiasi suono dovrebbe dissolversi gradualmente. Non rovinare le transizioni visive senza problemi con transizioni audio improvvise.
-   **I suoni devono essere nel formato di file WAV.** È consigliabile usare il formato stereo a 16 bit 44,1 kHz stereo non compresso Pulse Code Modulation (PCM). Se le dimensioni del file sono importanti, usare i formati compressi o mono (mono), ma tenere presente che esiste una perdita di qualità facilmente percepibile che potrebbe riflettere negativamente sull'applicazione.

### <a name="mixing"></a>Combinazione

-   **Non sono presenti controlli volume o mute nel programma.** Al contrario, consentire agli utenti di controllare le impostazioni del volume relativo tra le applicazioni con il mixer del volume di Windows. Se il programma dispone di un controllo del volume, saranno presenti più posizioni in cui gli utenti possono modificare le impostazioni, causando confusione.

    ![screenshot del mixer del volume di Windows ](images/vis-sound-image8.png)

    Il mixer del volume di Windows consente agli utenti di controllare l'impostazione principale del volume e il volume per ogni programma che sta attualmente eseguendo audio.

<!-- -->

-   **Eccezione:** Se lo scopo principale è la riproduzione o la riproduzione di audio o video, potrebbe essere utile disporre di un controllo volume nel programma. Usare un controllo dispositivo di scorrimento a questo scopo e fornire un feedback immediato quando l'utente modifica il volume.

### <a name="windows-integration"></a>Integrazione di Windows

-   **Registrare i suoni del programma nel registro suoni di Windows.** In questo modo, il mixer del volume di Windows può aggiungere un dispositivo di scorrimento per il programma.
-   **Registrare gli eventi audio personalizzati del programma.** Questa operazione consente all'elemento del pannello di controllo audio di Windows di visualizzarli. Creare la chiave seguente per ogni evento audio personalizzato: HKEY \_ Current \_ User \| AppEvents \| Event labels \| EventName = nome evento.
-   **Non hardwire i suoni per gli eventi audio del programma.** Specificare invece i suoni da riprodurre utilizzando le voci del registro di sistema. Questa operazione consente agli utenti di personalizzare gli eventi audio tramite l'elemento del pannello di controllo audio.
    -   **Eccezione:** È possibile scegliere di hardwire i suoni usati per la personalizzazione.
-   **Non fornire agli utenti un modo per configurare i suoni nelle opzioni del programma.** Usare invece l'elemento del pannello di controllo suoni Windows a questo scopo.
-   **Per impostazione predefinita, provare a non assegnare suoni agli eventi che si verificano di frequente.** Non è necessario che gli utenti configurino l'uscita da un'esperienza iniziale fastidiosa.

### <a name="directsound-programming-issues"></a>Problemi di programmazione DirectSound

-   Per i programmi DirectSound che dispongono di un proprio controllo del volume, **impostare il volume del programma su 100% per impostazione predefinita.** Questa operazione consente di massimizzare l'intervallo dinamico dell'audio.
-   **Non bloccare altri eventi audio eseguendo il programma in modalità esclusiva.** Questa operazione può impedire il corretto funzionamento di altri programmi. Ad esempio, l'uso della modalità esclusiva impedisce a un computer di essere utilizzato come dispositivo di telefonia.

## <a name="text"></a>Testo

-   Non usare la frase scheda audio. Usare invece la scheda audio.
-   Usare il dispositivo per fare riferimento in modo generico a altoparlanti, cuffie e microfoni.
-   Usare il controller per fare riferimento a hardware audio che controlla i dispositivi, ad esempio schede audio e chipset.
-   Utilizzare lo schema audio frase per descrivere una raccolta di suoni per gli eventi di programma comuni, ad esempio l'accesso o la ricezione di un nuovo messaggio di posta elettronica. Usare il tema del desktop frase per descrivere una raccolta di elementi visivi e suoni per il desktop del computer.
-   Usare il termine audio per fare riferimento a parole, musica e suoni. Usare il termine suono per fare riferimento in modo più restrittivo al programma e ai suoni di Windows descritti in questo articolo.

 

