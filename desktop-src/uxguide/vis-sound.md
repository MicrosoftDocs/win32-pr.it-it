---
title: Suoni
description: L'audio è l'elemento audio dell'esperienza utente.
ms.assetid: 2a276370-eff9-4844-b008-eba9ae5ac395
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5569fe76578fdb79b30da7cbad95939773889b0d22de92b0af4babe966ec6390
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348636"
---
# <a name="sound"></a>Suoni

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

*L'audio* è l'elemento audio dell'esperienza utente. Se usato in modo appropriato, il suono può essere una forma efficace di comunicazione che stabilisce una relazione non verbale e persino emotivo con gli utenti. I suoni possono essere usati da soli o come supplemento all'interfaccia utente visiva. Ad esempio, l'aggiunta di un effetto sonoro a una notifica aumenta la probabilità che verrà notata, soprattutto se l'utente non guarda lo schermo quando si verifica un evento.

![Screenshot della finestra di dialogo audio ](images/vis-sound-image1.png)

Dalla scheda Suoni dell'elemento Del pannello di controllo Audio gli utenti possono apportare modifiche ai suoni del sistema.

Questo articolo illustra l'uso dei suoni all'interno di un programma come risposta a eventi e azioni dell'utente e l'integrazione del controllo audio di un programma con Windows. Non tratta l'uso della musica o del parlato.

**Nota:** Le linee guida [relative alle notifiche](mess-notif.md) e alla [personalizzazione](exper-branding.md) sono presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere se usare l'audio, considerare queste domande:

-   **L'uso del suono è vantaggioso per l'utente?** Poiché gli svantaggi dell'uso del suono possono facilmente superare i vantaggi, usare il suono solo quando esiste un chiaro vantaggio.
-   **L'uso del suono è appropriato?** L'uso del suono richiama l'attenzione su elementi che sono di grande attenzione? Gli utenti perderebbero il suono se fosse assente? Concentrarsi sui suoni che tengono informati gli utenti, che probabilmente cambieranno il proprio comportamento o forniranno commenti e suggerimenti utili.
-   **L'uso del suono distrae?** Sono presenti suoni frequenti, ad alta voce e insodduranti? È probabile che gli utenti riducano il volume di sistema o il volume del programma in seguito all'uso del suono?
-   **Si sta usando il suono come forma principale di comunicazione?** In molti casi, ad esempio per gli utenti con un certo livello di perdita dell'udito, l'audio non deve essere usato come mezzo di comunicazione principale. L'audio è più efficace come integrazione ad altri mezzi di comunicazione, ad esempio testo o oggetti visivi.
-   **I principali utenti di destinazione sono i professionisti IT?** L'audio è in genere inefficace per le attività destinate ai professionisti IT perché molte delle loro attività vengono eseguite in modo automatico. Inoltre, il suono non viene ridimensionato per loro, immaginare l'esecuzione di centinaia di attività alla volta e la riproduzione di suoni quando vengono completati o non riescono.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

In genere l'audio ottiene uno o tutti gli scopi seguenti:

-   **Notifica.** L'audio può essere associato a eventi specifici. Ad esempio, un suono "nuovo messaggio di posta elettronica" indica agli utenti quando arriva la posta senza interrompere l'attività corrente.
-   **Valutazione.** L'audio può fornire commenti e suggerimenti per azioni utente specifiche. Ad esempio, un suono sottile che viene riprodotto quando si rilascia il dispositivo di scorrimento sul controllo del volume fornisce feedback sul livello dell'impostazione corrente.
-   **Branding.** L'audio può essere associato a contenuto specifico per il marchio del prodotto, dell'applicazione o del servizio. Windows l'audio in questo modo per l'avvio del sistema operativo.
-   **Intrattenimento.** Il suono viene comunemente usato per migliorare i prodotti di intrattenimento e per rendere i prodotti più coinvolgenti. Ad esempio, la maggior parte dei giochi, delle applicazioni di training e dei prodotti consumer usa il suono per insodettire gli utenti e migliorare l'esperienza.

Alcuni suoni possono soddisfare diversi di questi scopi contemporaneamente. Il Windows di avvio, ad esempio, indica che il processo di avvio è stato completato e che il desktop è pronto per l'uso. Offre anche una potente forma di personalizzazione del prodotto e coinvolge momentaneamente gli utenti.

I suoni che non soddisfano nessuno di questi scopi dovrebbero probabilmente essere eliminati.

### <a name="inappropriate-use-of-sound"></a>Uso inappropriato del suono

**Nonostante i vantaggi del suono, l'uso appropriato del suono richiede una notevole attenzione. In caso contrario, un programma può essere fastidioso e distrarre.** Gli utenti spegneranno completamente il suono se vengono infastiditi da suoni frequenti, ripetitivi, in jarring, che causano interruzioni, suoni progettati in modo non necessario; in parte perché, per sua natura, il suono richiede attenzione ed è difficile da ignorare. Per suggerimenti su come trovare un equilibrio ragionevole, vedere Linee guida per la progettazione [del suono.](#sound-design)

Poiché gli svantaggi dell'uso del suono possono facilmente superare i vantaggi, usare il suono solo quando esiste un chiaro vantaggio. **In caso di dubbi, non usare l'audio.**

### <a name="make-sound-supplemental"></a>Rendere il suono supplementare

Anche se il suono viene usato in modo appropriato, esistono molte situazioni in cui il suono potrebbe non essere efficace per tutti gli utenti:

-   Alcuni utenti potrebbero lavorare in un ambiente rumoroso in cui i suoni non possono essere uditi.
-   Alcuni utenti possono lavorare in un ambiente silenzioso che richiede che l'audio sia disattivato o impostato su un volume basso.
-   Alcuni utenti possono avere problemi di udito o perdita.
-   È possibile che il computer non abbia altoparlanti.

Per questi motivi, **l'audio usato** per le notifiche e il feedback non deve mai essere l'unico metodo di comunicazione, ma deve integrare segnali visivi o testuali.

### <a name="desirable-characteristics-of-sound"></a>Caratteristiche desiderabili del suono

In generale, i suoni devono essere:

-   frequenza medio-alta (da 600 Hertz \[ Hz \] a 2 kilohertz \[ \] kHz).
-   short (meno di un secondo).
-   soft o moderate nel volume.
-   Significativo.
-   non allarmismi o jarring.
-   non verbale.
-   non ripetitivo.

Con l'audio, meno è più. **L'effetto sonoro ideale è quello che gli utenti notano distorsi, ma che mancherebbero se fosse assente.**

**Un'errata concepizione comune è che i suoni per gli eventi critici devono essere forti e insodettiti per ottenere l'attenzione dell'utente.** Questo non è vero, perché l'audio è in realtà pensato per essere un mezzo di comunicazione supplementare. Nel caso di un messaggio di errore critico, la relativa presentazione (ad esempio in una finestra di dialogo modale), la relativa icona (icona di errore) e il testo e il tono si combinano per comunicare la natura dell'errore. Un suono di errore efficace può essere leggermente più alto rispetto al tipico Windows, ma non deve essere notevolmente più alto.

### <a name="characteristics-of-windows-sounds"></a>Caratteristiche dei Windows acustici

Oltre a questa richiesta generale per il minimalismo, l'acustica Windows usa suoni leggeri, puri e aridi e glassy, con una dissolvenza in entrata e una dissolvenza in uscita ("bordi" sfumati) per evitare effetti improvvi, jarring e percussivi. Sono progettate per essere sottintese, consonanti e consonanti. Windows suoni usano l'eco, il riverbero e l'equalizzazione per ottenere un aspetto naturale e ambientale.

Lo schema audio predefinito per Windows in genere non usa suoni quotidiani riconoscibili o riconoscibili che sono esempiamente specifici o meno. Esempi di suoni evitati sono strumenti acustici come piano o strumenti acustici, suoni di animali, rumori ambientali, voce, voci, effetti sonori simili a film o altri suoni di esseri umani. Inoltre, Windows suoni non sono concepiti per essere percepiti come musica( ovvero, a lungo, più note. Ciò rende Windows suoni dal punto di vista funzionale diversi da altri tipi di suoni.

Poiché i Windows sono stati progettati professionalmente in modo da avere le caratteristiche desiderate e accattivanti per un ampio pubblico, è consigliabile usare questi suoni Windows quando **appropriato.**

### <a name="designing-your-own-sounds"></a>Progettazione di suoni personalizzati

Se è necessario creare suoni personalizzati, progettarli in modo che abbia le caratteristiche descritte in precedenza. Cercare di renderli complementari alle attività o agli eventi associati.

Comprendere che la creazione di suoni originali è difficile da fare bene, soprattutto per i suoni destinati a un ampio pubblico. L'audio può essere un elemento di progettazione polarizzante. Per ogni utente che ami un suono, saranno molti quelli che lo non gradiranno.

**Progettare i suoni per il programma come gruppo in modo che siano varianti correlate di un tema.** L'esperienza di revisione del programma deve essere coordinata con l'esperienza visiva. Inoltre, il "tono" dei suoni deve essere coordinato con il [tono del testo](text-style-tone.md). Considerare il modo in cui il testo con un tono naturale e gradevole può essere danneggiato quando è accompagnato da suoni allarmismi.

**Se si eservino solo quattro operazioni...**

1.  Usare l'audio con una certa attenzione per assicurarsi che vi sia un chiaro vantaggio generale per l'utente. In caso di dubbi, non usare l'audio.
2.  Usare i suoni predefiniti Windows quando appropriato.
3.  Se si progettano suoni personalizzati, assicurarsi che abbia le caratteristiche sonore desiderabili e nel complesso si senta come variazioni su un tema.
4.  Non presupporre che i suoni devono essere forti e stridenti per ottenere l'attenzione dell'utente.

## <a name="usage-patterns"></a>Modelli di utilizzo

I suoni hanno diversi modelli di utilizzo:



|     Uso del suono                                                                                                                                                                 |  Esempio                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Completamento dell'azione**<br/> Notifica in modo simbolico agli utenti quando un'azione avviata dall'utente a esecuzione lunga viene completata correttamente. <br/>                             | ![Screenshot della finestra di dialogo di download del file ](images/vis-sound-image2.png)<br/> In questo esempio la finestra di dialogo riproduce un suono per notificare agli utenti che il download è stato completato.<br/>                                                                                                                                                                                                                                      |
| **Errore dell'azione**<br/> Notifica in modo simbolico agli utenti quando un'azione avviata dall'utente a esecuzione lunga ha esito negativo. <br/>                                                 | ![Screenshot del messaggio disco di backup non accessibile ](images/vis-sound-image3.png)<br/> In questo esempio, Windows un suono per notificare agli utenti che l'operazione di backup non è riuscita.<br/>                                                                                                                                                                                                                                  |
| **Evento di sistema importante**<br/> avvisa gli utenti di eventi di sistema importanti o di stato che richiedono un'attenzione immediata. <br/>                      | ![Screenshot del messaggio di batteria in esaurimento ](images/vis-sound-image4.png)<br/> In questo esempio gli utenti vengono avvisati che la batteria in esaurimento richiede un'attenzione immediata.<br/>                                                                                                                                                                                                                                                      |
| **Fyi**<br/> notifica in modo simbolico agli utenti informazioni potenzialmente utili e rilevanti. <br/>                                                                 | Poiché queste informazioni in genere non richiedono attenzione immediata, un suono fyi fornisce un feedback sottile senza interrompere il flusso dell'utente. <br/> ![Screenshot del messaggio di accesso live messenger ](images/vis-sound-image5.png)<br/> In questo esempio viene riprodotto un suono quando un contatto accede a un servizio di messaggistica immediata.<br/>                                                                                 |
| **Effetto sonoro**<br/> fornisce commenti e suggerimenti alle interazioni dell'utente. <br/>                                                                            | Fornisce un feedback sonoro reale o con stile appropriato per l'interazione. Gli effetti sonori spesso sonori come se l'utente manipola un oggetto fisico reale. a volte definito foley. <br/> ![Screenshot della finestra ridotta a icona ](images/vis-sound-image6.png)<br/> In questo esempio, l'effetto sonoro della finestra di riduzione a icona sembra che le dimensioni di un oggetto reale vengano ridotte.<br/> |
| **Suoni di personalizzazione**<br/> un suono fornito per migliorare l'esperienza utente anche se l'impatto emotivo e, come effetto collaterale, promuovere il marchio del prodotto. <br/> | I suoni di personalizzazione sono particolarmente utili quando vengono sincronizzati con gli eventi visivi, in particolare le transizioni dell'interfaccia utente, ad esempio la visualizzazione di una finestra del programma. I marchi sonori veri indicano l'origine dei beni, simili a una parola o un logo marchiati, e sono relativamente insoliti. <br/> ![Screenshot dell'icona di avvio di Windows ](images/vis-sound-image7.png)<br/> In questo esempio l Windows startup è un'esperienza di transizione personalizzata.<br/>      |



 

## <a name="guidelines"></a>Indicazioni

### <a name="usage"></a>Utilizzo

-   **Usare l'audio con restrizioni per** assicurarsi che sia disponibile un vantaggio generale per l'utente. Concentrarsi sui suoni che tengono informati gli utenti, probabilmente cambieranno il loro comportamento o forniranno feedback utili. In caso di dubbi, non usare il suono.
-   **Selezionare il suono e le relative caratteristiche in base al modo in cui viene usato.** Per una descrizione di ogni modello di utilizzo, vedere la tabella nella sezione precedente.
-   **Per le notifiche e i commenti e suggerimenti, non usare l'audio come unico metodo di comunicazione.** Usare invece il suono come metodo supplementare per rinforzare i segnali visivi o testuali. In questo modo si garantisce che gli utenti possano visualizzare le informazioni se non possono ascoltare il suono.
-   **Non riprodurre suoni rumorosi o difficili di frequente.** Questa operazione non è necessaria e comporta un'esperienza utente scadente. Più spesso viene riprodotto un suono, meno invadente dovrebbe essere. I suoni non devono essere forti o dure per attirare l'attenzione.
-   **Non esigono un segnale acustico.** Il beeping non è appropriato per i programmi moderni. I beeps non possono avere significati specifici assegnati e gli utenti non possono controllarli.
    -   **Eccezione:** Le funzioni di sistema critiche possono segnale acustico per avvisare gli utenti di situazioni a cui devono partecipare immediatamente, ad esempio l'alimentazione a batteria a basso consumo.

### <a name="playback"></a>Riproduzione

-   **Non ripetere un suono più di due volte consecutivamente.**
-   **Per una sequenza consecutiva di eventi sonori correlati, riprodurre un suono solo al primo evento.** Evitare di usare più suoni perché possono collidere tra loro o causare un'esperienza utente spiacevole.

### <a name="sound-selection"></a>Selezione del suono

-   **Scegliere suoni gradevoli.** Non usare suoni fastidiosi e allarmanti, ad esempio ronzio, arresto anomalo e interruzione.
-   **Usare suoni brevi** (meno di un secondo).
-   **Usare suoni approssimativamente dello stesso volume del tipico Windows audio.** Agli utenti non piace dover disattivare il volume quando si avvia un computer o un programma, in particolare in ambienti pubblici come riunioni e presentazioni. I file audio Windows Microsoft si trovano nella cartella Media all'interno della Windows file.
-   **Non scegliere suoni che richiedono la localizzazione.** È possibile ottenere questo risultato usando suoni che non usano il parlato o hanno significati o connotazioni dipendenti dalla cultura.

### <a name="windows-system-sounds"></a>Windows di sistema

-   **Usare i suoni di sistema Windows predefiniti quando appropriato.**
-   **Scegliere di usare i suoni di sistema in base al significato associato, non solo al suono stesso.** I suoni di sistema devono essere usati in modo coerente.

### <a name="sound-design"></a>Progettazione del suono

Quando si creano suoni personalizzati:

-   **Creare suoni con le caratteristiche sonore desiderabili.**
-   **Comporre suoni con frequenze per lo più medio-alte (da 600 Hz a 2 kHz).** Non usare frequenze basse perché viaggiano più lontano, sono più difficili da individuare e possono essere allarmanti.
-   **Impostare l'ampiezza relativa dei suoni normali sul livello del suono Windows normale.** I Windows sono stati livellati in modo appropriato per gli ambienti di lavoro e di casa. L'uso di livelli diversi per i suoni forza gli utenti a apportare modifiche al volume.
    -   Impostare suoni importanti in modo che siano leggermente più forti. Tali suoni includono i completamenti delle azioni, gli errori di azione e gli eventi di sistema importanti.
    -   Impostare i suoni che si verificano di frequente in modo che siano leggermente più soffi. Questi includono fYIs, suoni di personalizzazione ed effetti sonori.
-   **Scegliere i suoni coerenti con il significato Windows suoni.** Per creare una versione personalizzata di un suono Windows, mantenere lo stesso passo e lo stesso intervallo, ma modificare l'orchestrazione o il timbro. Non assegnare significati diversi ai suoni con altezze e intervalli simili Windows suoni.
-   **Progettare i suoni per il programma in modo che si senta come variazioni correlate in un tema.** L'esperienza udita del programma deve essere coordinata con l'esperienza visiva.
    -   **Progettare transizioni di scena e transizioni audio insieme.** Ad esempio, se una scena si dissolve gradualmente, anche qualsiasi suono dovrebbe dissolversi gradualmente. Non intralci le transizioni visive semplici con transizioni sonore improvrizzanti.
-   **I suoni devono essere in formato di file wav.** È consigliabile il formato PCM (Uncompressed Pulse Code Modulation) stereo a 16 bit a 44,1 kHz. Se le dimensioni del file sono importanti, usare formati compressi o monaurali (mono), ma tenere presente che si verifica una perdita di qualità facilmente individuabile che potrebbe riflettersi negativamente sull'applicazione.

### <a name="mixing"></a>Miscelazione

-   **Non sono presenti controlli di volume o disattivazione dell'audio nel programma.** Consentire invece agli utenti di controllare le impostazioni relative del volume tra le applicazioni Windows mixer di volumi. Se il programma ha un controllo del volume, gli utenti modificano le impostazioni in più posizioni, causando confusione.

    ![Screenshot del mixer di volumi di Windows ](images/vis-sound-image8.png)

    Il Windows mixer di volumi consente agli utenti di controllare l'impostazione del volume principale e il volume per ogni programma che sta riproducendo l'audio.

<!-- -->

-   **Eccezione:** Se lo scopo principale del programma è la riproduzione o la creazione di audio o video, può essere utile avere un controllo del volume nel programma. Usare un controllo dispositivo di scorrimento a questo scopo e fornire commenti e suggerimenti immediati quando l'utente modifica il volume.

### <a name="windows-integration"></a>Windows'integrazione

-   **Registrare i suoni del programma nel registro Windows Suoni.** Questa operazione consente al Windows mixer di volume di aggiungere un dispositivo di scorrimento per il programma.
-   **Registrare gli eventi audio personalizzati del programma.** Questa operazione consente all'Windows pannello di controllo Audio di visualizzarle. Creare la chiave seguente per ogni evento audio personalizzato: HKEY \_ CURRENT \_ USER \| AppEvents \| Event Labels \| EventName = Nome evento.
-   **Non eseguire il hardwire dei suoni per gli eventi sonori del programma.** Specificare invece i suoni da riprodurre usando le voci del Registro di sistema. In questo modo, gli utenti possono personalizzare gli eventi audio tramite l'elemento del pannello di controllo Audio.
    -   **Eccezione:** È possibile scegliere di eseguire il hardwire dei suoni usati per la personalizzazione.
-   **Non fornire agli utenti un modo per configurare i suoni all'interno delle opzioni del programma.** Usare invece l'elemento Windows pannello di controllo Suoni per questo scopo.
-   **Per impostazione predefinita, è consigliabile non assegnare suoni agli eventi che si verificano di frequente.** Non richiedere agli utenti di configurare la propria uscita da un'esperienza iniziale fastidiosa.

### <a name="directsound-programming-issues"></a>Problemi di programmazione di DirectSound

-   Per i programmi DirectSound con il proprio controllo del volume, impostare il volume del programma sul **100% per impostazione predefinita.** In questo modo si ottimizza l'intervallo dinamico dell'audio.
-   **Non bloccare altri eventi sonori eseguendo il programma in modalità esclusiva.** Questa operazione può impedire il corretto funzionamento di altri programmi. Ad esempio, l'uso della modalità esclusiva impedisce l'uso di un computer come dispositivo di telefonia.

## <a name="text"></a>Testo

-   Non usare l'adattatore audio per frasi. Usare invece la scheda audio.
-   Usare il dispositivo per fare riferimento genericamente a altoparlanti, cuffia e microfoni.
-   Usare il controller per fare riferimento all'hardware audio che controlla i dispositivi, ad esempio schede audio e chipset.
-   Usare lo schema sonoro per descrivere una raccolta di suoni per eventi comuni del programma, ad esempio l'accesso o la ricezione di nuovi messaggi di posta elettronica. Usare il tema del desktop della frase per descrivere una raccolta di elementi visivi e suoni per il desktop del computer.
-   Usare il termine audio per fare riferimento a voce, musica e suoni. Usare il termine suono per fare riferimento in modo più ristretto al programma e Windows suoni descritti in questo articolo.

 

