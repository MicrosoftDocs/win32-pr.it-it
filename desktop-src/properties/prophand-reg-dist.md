---
description: Questo articolo illustra come registrare e distribuire i gestori delle proprietà per l'uso con il sistema di proprietà di Windows.
ms.assetid: E6E81E04-9CC1-4df5-9A87-DE0CBD177356
title: Registrazione e distribuzione di gestori di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cffd6169ecbf371e49e27c555f468cdc03e2c3fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408344"
---
# <a name="registering-and-distributing-property-handlers"></a>Registrazione e distribuzione di gestori di proprietà

In questo argomento viene illustrato come creare e registrare gestori di proprietà da usare con il sistema di proprietà di Windows.

Questo argomento è organizzato come segue:

-   [Registrazione e distribuzione di gestori di proprietà](#registering-and-distributing-property-handlers)
-   [Considerazioni sulle prestazioni e sull'affidabilità per i gestori delle proprietà](#performance-and-reliability-considerations-for-property-handlers)
    -   [Linee guida per prestazioni e affidabilità](#guidelines-for-performance-and-reliability)
-   [Argomenti correlati](#related-topics)

## <a name="registering-and-distributing-property-handlers"></a>Registrazione e distribuzione di gestori di proprietà

Dopo l'implementazione, il gestore della proprietà deve essere registrato e la relativa estensione di file deve essere associata al gestore. L'esempio seguente che usa l'estensione .recipe illustra le voci del Registro di sistema necessarie a tale scopo.

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

I gestori delle proprietà per un particolare tipo di file vengono comunemente distribuiti con le applicazioni che creano o modificano file di tale tipo. È tuttavia consigliabile rendere disponibili i gestori delle proprietà indipendentemente da queste applicazioni per supportare l'indicizzazione del tipo di file negli scenari server in cui i gestori delle proprietà vengono usati dall'indicizzatore, ma le applicazioni che li accompagnano non sono necessarie. Se si crea un pacchetto di installazione autonomo per il gestore delle proprietà, assicurarsi che includa quanto segue:

-   Dettagli di registrazione del gestore delle proprietà specificati nell'argomento Registrazione e [distribuzione di gestori di proprietà]().
-   Registrazione per il tipo di file ed eventuali file di schema che devono essere installati, per consentire ai client di accedere a tutte le funzionalità del gestore delle proprietà.

## <a name="performance-and-reliability-considerations-for-property-handlers"></a>Considerazioni sulle prestazioni e sull'affidabilità per i gestori delle proprietà

I gestori delle proprietà vengono richiamati per ogni file in un computer specifico. In genere vengono chiamati nelle circostanze seguenti:

-   Durante l'indicizzazione del file. Questa operazione viene eseguita out-of-process, in un processo isolato con diritti limitati.
-   Quando si accede ai file in Esplora risorse allo scopo di leggere e scrivere valori di proprietà. Questa operazione viene eseguita in-process.

### <a name="guidelines-for-performance-and-reliability"></a>Linee guida per prestazioni e affidabilità

In qualsiasi momento, un utente potrebbe avere decine di migliaia di file di qualsiasi tipo specifico (incluso il proprio) nei propri computer e potrebbe accedere o modificare uno o tutti questi file in qualsiasi momento. Poiché i gestori delle proprietà vengono spesso richiamati per supportare queste operazioni di accesso e modifica, le caratteristiche di prestazioni e affidabilità del gestore delle proprietà negli ambienti occupati e altamente simultanei sono di importanza critica.

Tenere presenti le linee guida seguenti durante lo sviluppo e il test del gestore delle proprietà.

-   **Enumerazione delle proprietà**

    I gestori di proprietà devono avere un tempo di risposta molto rapido nell'enumerazione delle relative proprietà. È consigliabile evitare calcoli a elevato utilizzo di memoria dei valori delle proprietà, delle ricerche di rete o della ricerca di risorse diverse dal file stesso per garantire tempi di risposta rapidi.

-   **Scrittura di proprietà sul posto**

    Se possibile, quando si gestiscono file di medie dimensioni o di grandi dimensioni (diverse centinaia di KB o più grandi), il formato di file deve essere organizzato in modo che la lettura o la scrittura dei valori delle proprietà non richieda la lettura dell'intero file dal disco. Anche se è necessario cercare il file, non deve essere letto nella memoria nella sua interezza, perché ciò infetterà il working set di Esplora risorse o l'indicizzatore Windows Search mentre tentano di accedere a questi file o indicizzarlo. Per altre informazioni, vedere [Inizializzazione di gestori di proprietà](./building-property-handlers-property-handlers.md).

    Una tecnica utile per eseguire questa operazione consiste nel riempire l'intestazione del file con spazio aggiuntivo in modo che alla successiva scrittura di un valore di proprietà, il valore possa essere scritto sul posto senza dover riscrivere l'intero file. Questa operazione richiede la funzionalità ManualSafeSave. Questo approccio comporta un rischio aggiuntivo che l'operazione di scrittura di file possa essere interrotta mentre è in corso la scrittura (a causa di un arresto anomalo del sistema o di una perdita di alimentazione), ma poiché le dimensioni delle proprietà sono in genere ridotte, la probabilità di un'interruzione di questo tipo è analoga e i miglioramenti delle prestazioni che possono essere realizzati tramite la scrittura di proprietà sul posto sono considerati sufficientemente significativi da giustificare questo rischio aggiuntivo. Anche in questo caso, è necessario eseguire test approfonditi dell'implementazione per assicurarsi che i file non siano danneggiati nel caso in cui si verifica un errore nel corso di un'operazione di scrittura.

    Infine, quando si implementa la scrittura di proprietà sul posto con ManualSafeSave, talvolta l'operazione non può essere eseguita sul posto e l'intero flusso deve essere riscritto comunque. Per facilitare la riscrittura, il flusso fornito durante l'inizializzazione del gestore supporta [**l'interfaccia IDestinationStreamFactory.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) **L'interfaccia IDestinationStreamFactory** consente alle implementazioni del gestore di ottenere un flusso temporaneo per la scrittura. Quando tutte le scritture vengono completate e viene chiamato il metodo [**IDestinationStreamFactory::GetDestinationStream,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream) questo flusso viene usato per sostituire completamente il flusso di file originale. Quando viene usato il flusso di destinazione, il flusso di file originale deve essere considerato di sola lettura, perché verrà sostituito dal flusso di destinazione dopo la chiamata del metodo **IDestinationStreamFactory::GetDestinationStream.**

-   **Scelta del modello di threading COM**

    Per ottimizzare l'efficienza del gestore delle proprietà, è necessario specificare che usa il modello di threading COM `Both` . Ciò consente l'accesso diretto dagli apartment STA (Esplora risorse, ad esempio) e dagli apartment dell'agente di trasferimento messaggi (MTA), ad esempio il processo SearchProtocolHost in Windows Search, evitando il sovraccarico del marshalling in tali ambienti. Per ottenere il massimo vantaggio del modello di threading, è necessario designare anche tutti i servizi da cui dipende il gestore per evitare il marshalling nelle chiamate `Both` `Both` a tali componenti. Controllare la documentazione di questi servizi specifici per verificare se usano questo modello di threading.

-   **Concorrenza del gestore delle proprietà**

    I gestori di proprietà e [**l'interfaccia IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) sono progettati per l'accesso seriale anziché simultaneo. Esplora risorse, l'Windows Search indicizzatore e tutte le altre chiamate del gestore delle proprietà dalla codebase di Windows garantiscono questo utilizzo. Non deve esserci alcun motivo per cui terze parti usino contemporaneamente un gestore delle proprietà, ma questo comportamento non può essere garantito. Anche se è previsto che il modello di chiamata sia seriale, le chiamate possono essere effettuate su thread diversi, ad esempio quando l'oggetto viene chiamato in modalità remota tramite RPC COM, come avviene nell'indicizzatore. Pertanto, le implementazioni del gestore delle proprietà devono supportare la chiamata su thread diversi e idealmente non devono subire effetti negativi quando vengono chiamate contemporaneamente. Poiché il modello di chiamata previsto è seriale, un'implementazione semplice che usa una sezione critica dovrebbe essere sufficiente per soddisfare questi requisiti nella maggior parte dei casi. È accettabile evitare il blocco sulle chiamate simultanee usando la [**funzione TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) per rilevare e non eseguire chiamate simultanee.

-   **Concorrenza di file**

    I gestori delle proprietà vengono spesso usati in scenari in cui più applicazioni accedono a un file contemporaneamente. Di conseguenza, il gestore e le applicazioni devono gestire la concorrenza specificando le modalità di condivisione appropriate all'apertura del file. Devono anche essere a conoscenza dell'accesso specificato dalle altre applicazioni e di gestire i casi in cui l'accesso non è consentito. È meglio se tutti i consumer specificano modalità di condivisione liberista per consentire ad altri utenti di accedere al file contemporaneamente, ma quando si esegue questa operazione, è necessario gestire i problemi di coerenza. Le decisioni sulle modalità di condivisione più appropriate da usare devono essere prese nel contesto della community di applicazioni che accedono al file.

    I file system consentono alle applicazioni di aprire i file in modo da controllare se e come altre applicazioni possono aprire il file. Le modalità di condivisione consentono l'accesso in lettura, scrittura ed eliminazione. Il sistema di proprietà supporta un subset di queste modalità di condivisione, descritto nella tabella seguente.

    

    | Modalità di accesso                     | Modalità di condivisione                             |
    |---------------------------------|------------------------------------------|
    | Scrittura                           | Rifiutare altri lettori e writer           |
    | Scrittura (EnableShareDenyWrite)    | Abilitare altri lettori, negare altri writer |
    | Sola lettura (impostazione predefinita)             | Abilitare altri lettori, negare altri writer |
    | Sola lettura (EnableShareDenyNone) | Abilitare altri lettori e writer         |

    

     

    I gestori di proprietà aperti per **la scrittura** (GPS \_ READWRITE) negheranno altri lettori e writer. I gestori possono acconsentire esplicitamente al comportamento che consente ai lettori di specificare il flag (che implica `EnableShareDenyWrite` l'abilitazione della lettura) nella registrazione.

    Gestori di proprietà aperti per **la lettura** (IMPOSTAZIONE PREDEFINITA GPS), per impostazione predefinita \_ abilitano altri lettori ma negano altri writer. I gestori possono acconsentire esplicitamente all'abilitazione di altri writer specificando il `EnableShareDenyNone` flag nella relativa registrazione. Ciò significa che un gestore può gestire correttamente una situazione in cui il contenuto di un file cambia durante la lettura del file da parte del gestore.

    Per le definizioni dei flag, [**vedere GETPROPERTYSTOREFLAGS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui gestori delle proprietà](./building-property-handlers-properties.md)
</dt> <dt>

[Uso dei nomi dei tipi](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Uso degli elenchi di proprietà](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inizializzazione dei gestori di proprietà](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Procedure consigliate e domande frequenti sul gestore delle proprietà](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
