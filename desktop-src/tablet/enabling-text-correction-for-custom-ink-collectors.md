---
description: Pannello di input di Microsoft Tablet PC è uno strumento potente per l'immissione di testo scritto a mano con una penna e la correzione del testo senza l'uso di una tastiera.
ms.assetid: c45ac1b5-7713-4bcb-a130-4692cff99aa2
title: Abilitazione della correzione del testo per gli agenti di raccolta input penna personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accb0bf2129a4e93e543e3ec5cc73d3e65383dc57b581114f30e812b1ac88b8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940832"
---
# <a name="enabling-text-correction-for-custom-ink-collectors"></a>Abilitazione della correzione del testo per gli agenti di raccolta input penna personalizzati

Pannello di input di Microsoft Tablet PC è uno strumento potente per l'immissione di testo scritto a mano con una penna e la correzione del testo senza l'uso di una tastiera. Quando si usa il Pannello di input, un utente immette il testo tramite scrittura manuale sulle superfici di input penna del pannello di input, in modo che il Pannello di input riconosca la grafia dell'utente come testo. Dopo aver riconosciuto il testo, l'utente tocca Inserisci nel pannello di input per inserire il testo in un'applicazione o in un documento. Prima di inserire il testo, un utente può accedere a un set di strumenti di correzione nel Pannello input penna. Questi includono la selezione di un risultato di riconoscimento alternativo, la possibilità di riscrivere un singolo carattere o persino di riscrivere l'intera parola e riscriverla. Questi strumenti di correzione consentono all'utente di correggere sia gli errori di riconoscimento che gli errori umani.

Quando il testo immesso tramite il Pannello input penna è presente nel documento, gli utenti hanno accesso alla stessa funzionalità di correzione disponibile prima dell'inserimento nelle applicazioni basate su Windows [Framework servizi di testo](/windows/desktop/TSF/text-services-framework)e abilitate per Servizi di testo. A partire da Microsoft Windows XP Service Pack 2 Tablet PC Edition, tutte le applicazioni Rich Edit sono abilitate per i servizi di testo per impostazione predefinita e a partire da Windows Vista, le applicazioni HTML sono abilitate per impostazione predefinita. La correzione nel documento è disponibile solo nelle applicazioni basate sul servizio di testo e abilitate; Ciò è dovuto al fatto che il pannello input penna dipende dalla capacità del servizio di testo di archiviare le proprietà di testo associate, inclusi gli oggetti input penna e le alternative di riconoscimento, per fornire la correzione nel documento.

![Pannello di input di tablet PC con correzione del testo](images/a0dced5e-16de-410b-965f-5d97d297cee5.jpg)

Esistono tuttavia numerosi scenari, tra cui la correzione del riconoscimento vocale o la correzione di testo digitato in viaggio, che non iniziano con l'immissione di testo tramite il Pannello di input, ma in cui la correzione nel documento può essere estremamente utile per gli utenti di Tablet PC. Un esempio primo è nelle applicazioni che forniscono superfici input penna personalizzate per l'immissione di testo con una penna. Le superfici input penna personalizzate sono un ottimo modo per le applicazioni di fornire funzionalità personalizzate specifiche per le attività di immissione di testo di ogni applicazione. Inoltre, le superfici input penna personalizzate offrono un'esperienza utente di Tablet PC completamente integrata, che rende chiaro che la penna è un dispositivo di input di prima classe nelle applicazioni che li contengono. Tuttavia, le applicazioni che forniscono superfici input penna personalizzate potrebbero non consentire o non essere in grado di fornire lo stesso livello di supporto per la correzione disponibile nel Pannello di input nel documento.

![agente di raccolta input penna personalizzato](images/b6797b12-dda6-44c4-87f4-570fe0c23f3a.jpg)

Le applicazioni basate su Servizi di testo o abilitate in cui la correzione nel documento è utile per la correzione del testo non immesso tramite il pannello di input sono in grado di usare l'API [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) del pannello di input (classe [Microsoft.TextInput.HandwrittenTextInsertion](/previous-versions/ms573516(v=vs.100)) nel codice gestito) per abilitare la correzione nel documento per il testo immesso con altri mezzi. In questo modo, le applicazioni possono aggiungere economicamente un potente supporto per la correzione alle superfici di input penna personalizzate o ad altri scenari di immissione del testo e completare la storia di immissione testo in Tablet PC. L'API IHandWrittenTextInsertion del pannello di input è inclusa nel sistema operativo Windows Vista e come parte di Tablet Platform SDK versione 1.9 o successiva. Sono incluse sia una versione dell'API basata su .NET che su COM. L'abilitazione della correzione nel documento per il testo non immesso tramite il pannello di input è supportata Windows Vista e versioni più nuove. La correzione nel documento è disponibile solo per le lingue latini e non è in grado di visualizzare alcun carattere al di fuori del set di caratteri latini.

## <a name="how-to-use-the-handwrittentextinsertion-api-in-an-application"></a>Come usare l'API HandwrittenTextInsertion in un'applicazione

Le modifiche necessarie a un'applicazione per integrare la correzione nel documento del pannello di input per il testo non immesso tramite il pannello di input e l'API [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) sono semplici. Tutto il codice di immissione testo personalizzato dell'applicazione rimane invariato, ad eccezione dell'ultimo passaggio. Nel momento in cui il testo immesso usando una superficie input penna personalizzata, il riconoscimento vocale o altri mezzi deve essere visualizzato in un campo di testo abilitato per i servizi di testo, l'applicazione invia il testo all'interfaccia **IHandWrittenTextInsertion** anziché inviarlo direttamente al campo di testo. Il componente programmabilità pannello di input gestisce quindi l'inserimento del testo sia nel campo di testo che nell'archivio di backup dei servizi di testo. Quando si aggiunge il testo all'archivio di backup di Servizi di testo, il componente di programmabilità del pannello di input gestisce l'impostazione delle proprietà di testo richieste dal Pannello di input per l'ammissione della correzione nel documento per tale testo.

La sezione seguente illustra in dettaglio questo processo per un'applicazione C++ che usa la versione COM [**dell'API IHandWrittenTextInsertion.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) Sono disponibili note in qualsiasi punto in cui i passaggi per l'uso della .NET Framework dell'API in C differiscono per l'uso della versione \# COM in C++. L'API **gestita HandwrittenTextInsertion** include una singola interfaccia COM, **IHandwrittenTextInsertion.** La definizione per questa interfaccia si trova in PenInputPanel.h e PenInputPanel \_ i.c.

In primo luogo, l'applicazione deve usare la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per produrre un'istanza di [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) con ID classe **CLSID \_ HandwrittenTextInsertion**. Si noti che la creazione di un oggetto **CLSID \_ HandwrittenTextInsertion** avrà esito positivo solo dopo la creazione di una finestra e l'attivazione dello stato attivo, perché fino ad allora l'archivio di backup dei servizi di testo non è attivato. Inoltre, se tiptsf.dll non è presente nel sistema, la funzione **CoCreateInstance** ha esito negativo e restituisce **REGDB \_ E \_ CLASSNOTREG,** a indicare che la correzione del pannello di input nel documento non è supportata nel sistema. A questo punto l'applicazione deve procedere senza tentare di abilitare la correzione del pannello di input nel documento. L'istanza **di HandwrittenTextInsertion** deve essere accessibile dal codice dell'applicazione che gestisce l'inserimento di testo in un campo di testo.

> [!Note]  
> Quando si usa la versione .NET Framework dell'API, l'applicazione deve aggiungere un'istruzione using per consentire l'accesso allo spazio dei nomi [Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) e quindi creare l'oggetto direttamente.

 

In secondo momento, il codice dell'applicazione responsabile dell'inserimento di testo in un campo di testo deve essere modificato in modo che non inserisca più testo direttamente in un campo di testo, ma chiama invece uno o l'altro dei due metodi di inserimento di [**IHandwrittenTextInsertion.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) Se le applicazioni devono scegliere di chiamare [**InsertRecognitionResultsArray**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertrecognitionresultsarray) o [**InsertRecognitionResults**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertinkrecognitionresult) dipende dal fatto che l'applicazione abbia le alternative di riconoscimento per il testo archiviato come matrice o come oggetto [**IInkRecognitionResult.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)

> [!Note]  
> Quando si lavora nel codice gestito, l'oggetto riconoscimento corrispondente utilizzato da InsertRecognitionResultsArray è [RecognitionResult.](/previous-versions/ms552537(v=vs.100)) Entrambi i metodi utilizzano i tre parametri seguenti:

 

-   *alternative* Raccolta bidimensionale di stringhe, archiviata come matrice di matrici o come oggetto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) (o [RecognitionResult).](/previous-versions/ms552537(v=vs.100)) Se le alternative vengono archiviate come matrice di matrici, devono essere passate come puntatore di matrice sicuro. Ogni voce nella matrice di primo livello è un elenco di alternative per una singola parola nell'inserimento. La voce nella posizione zero nelle sottomatrici di alternative è il testo inserito nel campo di testo. Le alternative aggiuntive (indici da 1 a n in ogni sottomatrici) vengono archiviate nell'archivio di backup dei servizi di testo e offerte all'utente come scelte come parte della correzione nel documento. Se non sono incluse alternative, l'utente visualizza "Nessun suggerimento" al posto dell'elenco delle alternative. Se un inserimento contiene più parole con spazi tra di esse, ogni spazio deve essere incluso come voce nella matrice di primo livello.
-   *lingua* LCID [della lingua di](/previous-versions/ms221397(v=vs.71)) input che corrisponde al testo contenuto nel *parametro alternates.* Nel caso in cui  il contenuto delle alternative sia stato generato da un riconoscimento vocale o grafia, questa è anche la proprietà [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) associata al riconoscimento usato.
-   *fLatticeContainsAutoSpacingInformation* Flag che indica se il testo contenuto nel parametro *alternates* è stato generato da un sistema di riconoscimento con la spaziatura automatica abilitata. Se la spaziatura automatica è stata abilitata, il flag deve essere impostato su **TRUE.** Se la spaziatura automatica è stata disabilitata, il flag deve essere impostato su **FALSE.** Nel caso in cui  il contenuto delle alternative sia stato generato da un sistema di riconoscimento che non supporta la spaziatura automatica o che non è stato generato da un riconoscitore, il flag deve essere impostato su **FALSE.**

Il modello di programmabilità del pannello di input è in grado di inserire il testo nel documento o nell'applicazione dalla posizione del cursore di sistema.

Entrambi i metodi restituiscono **S \_ OK** se l'inserimento ha esito positivo. Restituiscono **E \_ NOINTERFACE** se l'applicazione non è basata su  Servizi di testo o è abilitata ed **E \_ INVALIDARG** se le alternative sono formattate in modo non corretto o inaccessibili. Possono anche restituire **E \_ OUTOFMEMORY** se la memoria disponibile nel sistema non è sufficiente oppure **E \_ FAIL** dopo un errore irreversibile, ad esempio se il Framework servizi di testo non è abilitato.

### <a name="conclusion"></a>Conclusione

L'abilitazione della correzione nel documento del pannello di input per il testo non immesso tramite il pannello di input è un modo semplice e economico per un'applicazione basata su Servizi di testo o abilitata per integrare un input penna personalizzato o un metodo di input con funzionalità avanzate di correzione basata su penna. In Windows Vista tutte le applicazioni Rich Edit e Trident sono abilitate per i servizi di testo. Anche se le superfici input penna integrate sono un'ottima opzione per l'aggiunta di un'esperienza utente personalizzata di Tablet PC a un'applicazione, supportano solo metà dell'immissione di testo se non includono funzionalità di correzione. La correzione nel documento offre agli utenti l'altra metà del brano aggiungendo la possibilità di scambiare una selezione con un'alternativa di riconoscimento o di riscrivere parte o tutta la selezione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione del pannello input di testo](programming-the-text-input-panel.md)
</dt> </dl>

 

 
