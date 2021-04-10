---
description: In questo argomento viene illustrato come creare e registrare gestori di proprietà per utilizzare il sistema di proprietà di Windows.
ms.assetid: E6E81E04-9CC1-4df5-9A87-DE0CBD177356
title: Registrazione e distribuzione di gestori di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1de6af17df8e15912870626935995c67c25f518
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226891"
---
# <a name="registering-and-distributing-property-handlers"></a>Registrazione e distribuzione di gestori di proprietà

In questo argomento viene illustrato come creare e registrare gestori di proprietà per utilizzare il sistema di proprietà di Windows.

Questo argomento è organizzato nel modo seguente:

-   [Registrazione e distribuzione di gestori di proprietà](#registering-and-distributing-property-handlers)
-   [Considerazioni sulle prestazioni e sull'affidabilità per i gestori di proprietà](#performance-and-reliability-considerations-for-property-handlers)
    -   [Linee guida per le prestazioni e l'affidabilità](#guidelines-for-performance-and-reliability)
-   [Argomenti correlati](#related-topics)

## <a name="registering-and-distributing-property-handlers"></a>Registrazione e distribuzione di gestori di proprietà

Una volta implementato, il gestore delle proprietà deve essere registrato e l'estensione del nome file deve essere associata al gestore. L'esempio seguente che usa l'estensione Recipe illustra le voci del registro di sistema necessarie a tale scopo.

```
HKEY_CLASSES_ROOT
   CLSID
      {50d9450f-2a80-4f08-93b9-2eb526477d1a}
         (Default) = Recipe Property Handler
         ManualSafeSave [REG_DWORD] = 00000001
         InProcServer32
            (Default) = C:\\SDK\\PropertyHandlerSample\\bin\\RecipeHandlers.dll
            ThreadingModel = Apartment
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     .recipe
                        (Default) = {50d9450f-2a80-4f08-93b9-2eb526477d1a}
```

I gestori di proprietà per un determinato tipo di file vengono in genere distribuiti con le applicazioni che creano o modificano i file di quel tipo. Tuttavia, è consigliabile rendere disponibili i gestori delle proprietà indipendentemente da queste applicazioni per supportare l'indicizzazione del tipo di file in scenari server in cui i gestori di proprietà vengono utilizzati dall'indicizzatore, ma le applicazioni associate non sono necessarie. Se si crea un pacchetto di installazione autonomo per il gestore delle proprietà, assicurarsi che includa quanto segue:

-   I dettagli di registrazione del gestore di proprietà specificati nell'argomento [registrazione e distribuzione di gestori di proprietà]().
-   Registrazione per il tipo di file e i file di schema che devono essere installati, per consentire ai client di accedere a tutte le funzionalità del gestore della proprietà.

## <a name="performance-and-reliability-considerations-for-property-handlers"></a>Considerazioni sulle prestazioni e sull'affidabilità per i gestori di proprietà

I gestori di proprietà vengono richiamati per ogni file in un particolare computer. Vengono in genere chiamati nei casi seguenti:

-   Durante l'indicizzazione del file. Questa operazione viene eseguita out-of-process in un processo isolato con diritti limitati.
-   Quando si accede ai file in Esplora risorse per la lettura e la scrittura dei valori delle proprietà. Questa operazione viene eseguita in-process.

### <a name="guidelines-for-performance-and-reliability"></a>Linee guida per le prestazioni e l'affidabilità

In qualsiasi momento, è possibile che un utente disponga di decine di migliaia di file di qualsiasi tipo specifico (incluso il proprio) nei propri computer e possa accedere o modificare uno o tutti i file in qualsiasi momento. Poiché i gestori delle proprietà vengono richiamati di frequente per supportare le operazioni di accesso e modifica, le caratteristiche di prestazioni e affidabilità del gestore di proprietà in ambienti occupati e altamente simultanei sono di importanza critica.

Tenere presenti le linee guida seguenti durante lo sviluppo e il test del gestore della proprietà.

-   **Enumerazione Property**

    I gestori di proprietà devono avere un tempo di risposta molto rapido nell'enumerazione delle relative proprietà. I calcoli con utilizzo intensivo della memoria dei valori delle proprietà, delle ricerche di rete o la ricerca di risorse diverse da quelle del file devono essere evitati per assicurare tempi di risposta rapidi.

-   **Scrittura di proprietà sul posto**

    Se possibile, quando si gestiscono file di medie o grandi dimensioni (diverse centinaia di KB), il formato del file deve essere disposto in modo che i valori delle proprietà di lettura o scrittura non richiedano la lettura dell'intero file dal disco. Anche se il file deve essere cercato, non deve essere letto in memoria per intero, perché il working set di Esplora risorse o l'indicizzatore di Windows Search tenta di accedere a questi file o di indicizzarli. Per ulteriori informazioni, vedere [inizializzazione dei gestori di proprietà](./building-property-handlers-property-handlers.md).

    Una tecnica utile per eseguire questa operazione consiste nel riempire l'intestazione del file con spazio aggiuntivo, in modo che la volta successiva in cui deve essere scritto un valore di proprietà, il valore possa essere scritto sul posto senza dover riscrivere l'intero file. Questa operazione richiede la funzionalità ManualSafeSave. Questo approccio comporta un ulteriore rischio che l'operazione di scrittura di file venga interrotta mentre è in corso la scrittura (a causa di un arresto anomalo del sistema o della perdita di energia), ma poiché le dimensioni delle proprietà sono in genere limitate, la probabilità di tale interruzione è analoga e il miglioramento delle prestazioni che può essere realizzato tramite la scrittura di proprietà sul posto è considerato abbastanza significativo per giustifica Anche in questo caso, è necessario prestare attenzione a testare l'implementazione in modo esteso per assicurarsi che i file non siano danneggiati nel caso in cui si verifichi un errore nel corso di un'operazione di scrittura.

    Infine, quando si implementa la scrittura della proprietà sul posto con ManualSafeSave, a volte l'operazione non può essere eseguita sul posto e l'intero flusso deve comunque essere riscritto. Per semplificare la riscrittura, il flusso fornito durante l'inizializzazione del gestore supporta l'interfaccia [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) . L'interfaccia **IDestinationStreamFactory** consente alle implementazioni del gestore di ottenere un flusso temporaneo per la scrittura. Quando tutte le scritture vengono completate e viene chiamato il metodo [**IDestinationStreamFactory:: GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream) , questo flusso viene usato per sostituire completamente il flusso di file originale. Quando viene usato il flusso di destinazione, il flusso di file originale deve essere considerato di sola lettura, in quanto verrà sostituito dal flusso di destinazione dopo la chiamata al metodo **IDestinationStreamFactory:: GetDestinationStream** .

-   **Scelta del modello di threading COM**

    Per ottimizzare l'efficienza del gestore delle proprietà, è necessario specificare che venga utilizzato il modello di threading COM `Both` . Ciò consente l'accesso diretto da apartment STA (ad esempio, Esplora risorse, ad esempio) e gli Apartment di agente di trasferimento messaggi (MTA) (il processo SearchProtocolHost in Windows Search, ad esempio), evitando il sovraccarico del marshalling in tali ambienti. Per ottenere l'intero vantaggio del `Both` modello di threading, è necessario designare anche tutti i servizi da cui dipende il gestore, come `Both` per evitare qualsiasi marshalling nelle chiamate a tali componenti. Controllare la documentazione di questi servizi specifici per verificare se utilizzano il modello di Threading.

-   **Concorrenza del gestore delle proprietà**

    I gestori di proprietà e l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) sono progettati per l'accesso seriale anziché simultaneo. Esplora risorse, l'indicizzatore di ricerca di Windows e tutte le altre chiamate ai gestori di proprietà dalla codebase di Windows garantiscono questo utilizzo. Non è necessario che le terze parti usino contemporaneamente un gestore di proprietà, ma questo comportamento non può essere garantito. Inoltre, anche se il modello di chiamata deve essere seriale, le chiamate possono provenire su thread diversi, ad esempio quando l'oggetto viene chiamato in modalità remota tramite la RPC COM, come avviene nell'indicizzatore. Pertanto, le implementazioni del gestore delle proprietà devono supportare la chiamata su thread diversi e, idealmente, non dovrebbero soffrire di effetti negativi quando vengono chiamati simultaneamente. Poiché il modello di chiamata designato è seriale, un'implementazione banale che usa una sezione critica dovrebbe essere sufficiente per soddisfare questi requisiti nella maggior parte dei casi. È accettabile evitare il blocco delle chiamate simultanee usando la funzione [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) per rilevare e interrompere le chiamate simultanee.

-   **Concorrenza di file**

    I gestori di proprietà vengono spesso utilizzati negli scenari in cui più applicazioni accedono contemporaneamente a un file. Di conseguenza, il gestore e le applicazioni devono gestire la concorrenza specificando le modalità di condivisione appropriate durante l'apertura del file. Devono inoltre essere consapevoli dell'accesso specificato dalle altre applicazioni e per gestire i casi in cui l'accesso non è consentito. È consigliabile che tutti i consumer specifichino le modalità di condivisione liberali per consentire ad altri utenti di accedere al file contemporaneamente, ma in questo caso è necessario gestire i problemi di coerenza. Le decisioni relative alle modalità di condivisione più appropriate da usare devono essere eseguite nel contesto della community di applicazioni che accedono al file.

    I file System consentono alle applicazioni di aprire i file in modo da controllare se e come altre applicazioni possono aprire il file. Le modalità di condivisione consentono l'accesso in lettura, scrittura ed eliminazione. Il sistema di proprietà supporta un subset di queste modalità di condivisione, illustrato nella tabella seguente.

    

    | Modalità di accesso                     | Modalità di condivisione                             |
    |---------------------------------|------------------------------------------|
    | Scrittura                           | Nega altri Reader e writer           |
    | Scrittura (EnableShareDenyWrite)    | Abilitare altri lettori, negare ad altri writer |
    | Sola lettura (impostazione predefinita)             | Abilitare altri lettori, negare ad altri writer |
    | Sola lettura (EnableShareDenyNone) | Abilita altri Reader e writer         |

    

     

    I gestori di proprietà aperti per la **scrittura** ( \_ ReadWrite GPS) negano ad altri Reader e writer. I gestori possono scegliere il comportamento che consente ai lettori specificando il `EnableShareDenyWrite` flag (che implica l'abilitazione della lettura) nella registrazione.

    I gestori di proprietà aperti per la **lettura** ( \_ impostazione predefinita GPS), per impostazione predefinita consentono ad altri lettori di negare altri writer. I gestori possono scegliere di abilitare altri writer specificando il `EnableShareDenyNone` flag nella registrazione. Ciò significa che un gestore può gestire correttamente una situazione in cui il contenuto di un file cambia mentre il gestore legge il file.

    Per le definizioni dei flag, vedere [**GETPROPERTYSTOREFLAGS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui gestori delle proprietà](./building-property-handlers-properties.md)
</dt> <dt>

[Uso dei nomi dei tipi](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Uso degli elenchi di proprietà](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inizializzazione di gestori di proprietà](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Procedure consigliate e domande frequenti sul gestore delle proprietà](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
