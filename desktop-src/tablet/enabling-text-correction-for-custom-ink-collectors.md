---
description: Il pannello di input di Microsoft Tablet PC è uno strumento potente per l'immissione di testo scritto a mano con una penna e la correzione del testo senza utilizzare una tastiera.
ms.assetid: c45ac1b5-7713-4bcb-a130-4692cff99aa2
title: Abilitazione della correzione del testo per gli agenti di raccolta input penna personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4dee4c7dfee1489cd002848c496be41f73d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561371"
---
# <a name="enabling-text-correction-for-custom-ink-collectors"></a>Abilitazione della correzione del testo per gli agenti di raccolta input penna personalizzati

Il pannello di input di Microsoft Tablet PC è uno strumento potente per l'immissione di testo scritto a mano con una penna e la correzione del testo senza utilizzare una tastiera. Quando si usa il pannello di input, un utente immette il testo in base alla grafia sulle superfici di Inking del pannello di input, che fa sì che il pannello di input riconosca la grafia dell'utente come testo. Una volta riconosciuto il testo, l'utente tocca Inserisci sul pannello input per inserire il testo in un'applicazione o in un documento. Prima di inserire il testo, un utente ha accesso a un set di strumenti di correzione nel Pannello input. Sono incluse la selezione di un risultato di riconoscimento alternativo, la possibilità di riscrivere un singolo carattere o persino di riscrivere l'intera parola e di riscrivere. Questi strumenti di correzione consentono a un utente di correggere sia errori di riconoscimento che errori umani.

Una volta che il testo immesso utilizzando il pannello input è presente nel documento, gli utenti hanno accesso alla stessa funzionalità di correzione disponibile prima dell'inserimento in applicazioni Windows [Text Services](/windows/desktop/TSF/text-services-framework)basate su Framework e servizi di testo. A partire da Microsoft Windows XP Service Pack 2 Tablet PC Edition tutte le applicazioni Rich Edit sono abilitate per i servizi di testo per impostazione predefinita e, a partire da Windows Vista, le applicazioni HTML sono abilitate per i servizi di testo per impostazione predefinita. La correzione nel documento è disponibile solo in applicazioni basate su servizi di testo e abilitate; Questo è dovuto al fatto che il pannello di input dipende dalla capacità del servizio di testo di archiviare le proprietà del testo associate, inclusi oggetti Ink e alternative di riconoscimento, per fornire la correzione nel documento.

![Pannello di input di Tablet PC con correzione del testo](images/a0dced5e-16de-410b-965f-5d97d297cee5.jpg)

Esistono, tuttavia, numerosi scenari, tra cui la correzione del riconoscimento vocale o la correzione del testo tipizzato in go, che non inizia con una voce di testo che usa il pannello di input, ma in cui la correzione in-Document può essere estremamente utile per gli utenti di Tablet PC. Un esempio principale è costituito da applicazioni che forniscono superfici di input personalizzate per l'immissione di testo tramite una penna. Le superfici di Inking personalizzate sono un ottimo modo per offrire alle applicazioni funzionalità personalizzate specifiche per le attività di immissione di testo di ogni applicazione. Inoltre, le superfici di Inking personalizzate forniscono un'esperienza utente di Tablet PC completamente integrata che rende chiaro che la penna è un dispositivo di input di prima classe nelle applicazioni che le contengono. Tuttavia, le applicazioni che forniscono superfici di Inking personalizzate potrebbero non consentire o potrebbe non essere in grado di fornire lo stesso livello di supporto per la correzione disponibile dalla correzione del pannello di input nel documento.

![agente di raccolta input penna personalizzato](images/b6797b12-dda6-44c4-87f4-570fe0c23f3a.jpg)

Le applicazioni basate su servizi di testo o abilitate in cui la correzione nel documento è utile per la correzione del testo non immesso tramite il pannello di input è in grado di utilizzare l'API [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) del pannello di input (classe [Microsoft. TextInput. HandwrittenTextInsertion](/previous-versions/ms573516(v=vs.100)) nel codice gestito) per abilitare la correzione nel documento per il testo immesso in altro modo. In questo modo, le applicazioni possono aggiungere in modo economico un potente supporto per la correzione alle superfici di inserimenti personalizzate o ad altri scenari di immissione di testo e arrotondare la storia della voce di testo di Tablet PC. L'API IHandWrittenTextInsertion del pannello di input è inclusa come parte del sistema operativo Windows Vista e come parte di Tablet Platform SDK versione 1,9 o successiva. Sono incluse sia una versione .NET che una versione basata su COM dell'API. L'abilitazione della correzione nel documento per il testo non immesso utilizzando il pannello input è supportata in Windows Vista e versioni successive. La correzione nel documento è disponibile solo per le lingue latine e non è in grado di visualizzare alcun carattere al di fuori del set di caratteri latini.

## <a name="how-to-use-the-handwrittentextinsertion-api-in-an-application"></a>Come usare l'API HandwrittenTextInsertion in un'applicazione

Le modifiche richieste a un'applicazione per integrare la correzione del pannello di input nel documento per il testo non immesso tramite il pannello input e l'uso dell'API [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) sono semplici. Tutto il codice di immissione di testo personalizzato dell'applicazione rimane invariato ad eccezione dell'ultimo passaggio. Nel momento in cui il testo immesso usando un'area di Inking personalizzata, il riconoscimento vocale o altri mezzi deve essere visualizzato in un campo di testo abilitato per i servizi di testo, l'applicazione invia il testo all'interfaccia **IHandWrittenTextInsertion** anziché inviarlo direttamente al campo di testo. Il componente di programmabilità del pannello di input gestisce quindi l'inserimento del testo nel campo di testo e nell'archivio di backup dei servizi di testo. Quando si aggiunge il testo all'archivio di backup dei servizi di testo, il componente di programmabilità del pannello di input gestisce l'impostazione delle proprietà di testo richieste dal pannello di input per la correzione nel documento da abilitare per tale testo.

La sezione seguente illustra in dettaglio questo processo per un'applicazione C++ che usa la versione COM dell'API [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) . Ci sono alcune note in cui i passaggi per l'uso della versione .NET Framework dell'API in C sono \# diversi per la versione di using com in C++. L'API **HandwrittenTextInsertion** gestita include una singola interfaccia com, **IHandwrittenTextInsertion**. La definizione per questa interfaccia si trova in PenInputPanel. h e PenInputPanel \_ i.c.

In primo luogo, l'applicazione deve utilizzare la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per produrre un'istanza di [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) con ID di classe **CLSID \_ HandwrittenTextInsertion**. Si noti che la creazione di un oggetto **\_ HandwrittenTextInsertion CLSID** avrà esito positivo solo dopo la creazione di una finestra e l'attivazione dello stato attivo, perché fino a quel momento non viene attivato il back-Store dei servizi di testo. Inoltre, se tiptsf.dll non è presente nel sistema, la funzione **CoCreateInstance** ha esito negativo e restituisce **REGDB \_ e \_ CLASSNOTREG**, che indica che la correzione nel documento del pannello di input non è supportata nel sistema. A questo punto l'applicazione deve procedere senza tentare di abilitare la correzione del pannello di input nel documento. L'istanza di **HandwrittenTextInsertion** deve essere accessibile dal codice dell'applicazione che gestisce l'inserimento di testo in un campo di testo.

> [!Note]  
> Quando si utilizza la versione .NET Framework dell'API, l'applicazione deve aggiungere un'istruzione using per consentire l'accesso allo spazio dei nomi [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) , quindi creare direttamente l'oggetto.

 

In secondo luogo, è necessario modificare il codice dell'applicazione responsabile dell'inserimento di testo in un campo di testo in modo che non inserisca più testo in un campo di testo direttamente, ma chiami invece uno o l'altro dei due metodi di inserimento di [**IHandwrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion). Il fatto che le applicazioni scelgano di chiamare [**InsertRecognitionResultsArray**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertrecognitionresultsarray) o [**InsertRecognitionResults**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertinkrecognitionresult) dipenda dal fatto che l'applicazione disponga delle alternative di riconoscimento per il testo archiviato come matrice o come oggetto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .

> [!Note]  
> Quando si utilizza codice gestito, l'oggetto di riconoscimento corrispondente utilizzato da InsertRecognitionResultsArray è [RecognitionResult](/previous-versions/ms552537(v=vs.100)). Entrambi i metodi utilizzano i seguenti tre parametri:

 

-   *alternative* È una raccolta bidimensionale di stringhe, archiviata come matrice di matrici o come oggetto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) (o [RecognitionResult](/previous-versions/ms552537(v=vs.100))). Se le alternative vengono archiviate come matrice di matrici, devono essere passate come puntatore di matrice sicuro. Ogni voce nella matrice di primo livello è un elenco di alternative per una singola parola nell'inserimento. La voce nella posizione zero nelle sottomatrici di alternative è il testo inserito nel campo di testo. Le alternative aggiuntive (indici da 1 a n in ogni sottomatrice) vengono archiviate nell'archivio di backup dei servizi di testo e offerte all'utente come parte della correzione nel documento. Se le alternative non sono incluse, l'utente visualizza ' nessun suggerimento ' al posto dell'elenco di alternative. Se un inserimento contiene più parole con spazi tra di essi, ogni spazio deve essere incluso come una voce nella matrice di primo livello.
-   *lingua* di [Identificatore LCID](/previous-versions/ms221397(v=vs.71)) della lingua di input corrispondente al testo contenuto nel parametro *alternates* . Nel caso in cui il contenuto delle *alternative* sia stato generato da un riconoscimento della grafia o dalla sintesi vocale, si tratta anche della proprietà [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) associata al riconoscimento usato.
-   *fLatticeContainsAutoSpacingInformation* Flag che indica se il testo contenuto nel parametro *alternates* è stato generato da un riconoscimento con spaziatura automatica abilitata. Se è stata abilitata la spaziatura automatica, il flag deve essere impostato su **true**. Se la spaziatura automatica è stata disabilitata, il flag deve essere impostato su **false**. Nel caso in cui il contenuto delle *alternative* sia stato generato da un riconoscimento che non supporta la spaziatura automatica oppure non è stato generato da un riconoscimento, il flag deve essere impostato su **false**.

Il modello di programmabilità del pannello di input è in grado di inserire il testo nel documento o nell'applicazione dalla posizione del punto di inserimento del sistema.

Entrambi i metodi restituiscono **\_ OK** se l'inserimento ha esito positivo. Restituiscono **e \_ nointerface** se l'applicazione non è basata su servizi di testo o abilitato e e **\_ INVALIDARG** se le *alternative* sono formattate in modo errato o non sono accessibili. Potrebbero inoltre restituire **E \_ OutOfMemory** se la memoria disponibile nel sistema non è sufficiente oppure E si verifica **un \_** errore irreversibile, ad esempio il Framework di servizi di testo non abilitato.

### <a name="conclusion"></a>Conclusione

L'abilitazione della correzione del pannello di input nel documento per il testo non immesso tramite il pannello input è un modo semplice e veloce per un'applicazione basata su servizi di testo o abilitata per integrare un metodo di input o di input personalizzato con funzionalità di correzione basate su penna avanzate. In Windows Vista, tutte le applicazioni Rich Edit e Trident sono abilitate per i servizi di testo. Sebbene le superfici di Inking integrate siano un'ottima opzione per l'aggiunta di un'esperienza utente personalizzata per Tablet PC a un'applicazione, sono supportate solo metà della voce di testo se non includono funzionalità di correzione. La correzione nel documento consente agli utenti di usare l'altra metà della storia aggiungendo la possibilità di scambiare una selezione per un'alternativa di riconoscimento o di riscrivere parte o tutta la selezione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione del pannello input di testo](programming-the-text-input-panel.md)
</dt> </dl>

 

 
