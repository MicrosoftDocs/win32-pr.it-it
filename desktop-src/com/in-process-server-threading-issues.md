---
title: Problemi di threading del server In-Process
description: Problemi di threading del server In-Process
ms.assetid: 7bd6f62f-8c91-44bd-9a7f-d47988180eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d02af739eac11a6adae62de76be9078ee8e32
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104399919"
---
# <a name="in-process-server-threading-issues"></a>Problemi di threading del server In-Process

Un server in-process non chiama [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize), [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)o [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) per contrassegnare il modello di Threading. Per gli oggetti basati su DLL o in-process compatibili con i thread, è necessario impostare il modello di threading nel registro di sistema. Il modello predefinito quando non si specifica un modello di threading è a thread singolo per processo. Per specificare un modello, aggiungere il valore **ThreadingModel** alla chiave [InprocServer32](inprocserver32.md) nel registro di sistema.

Le dll che supportano la creazione di un'istanza di un oggetto classe devono implementare ed esportare le funzioni [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) e [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow). Quando un client desidera un'istanza della classe supportata dalla DLL, una chiamata a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (direttamente o tramite una chiamata a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) chiama **DllGetClassObject** per ottenere un puntatore all'oggetto classe quando l'oggetto viene implementato in una dll. **DllGetClassObject** deve pertanto essere in grado di fornire più oggetti classe o un singolo oggetto thread-safe (essenzialmente utilizzando [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) / [**InterlockedDecrement**](/windows/desktop/api/winbase/nf-winbase-interlockeddecrement) sui rispettivi conteggi dei riferimenti interni).

Come suggerisce il nome, viene chiamato [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow) per determinare se la dll che lo implementa è in uso, consentendo al chiamante di scaricarla in modo sicuro in caso contrario. Le chiamate a [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) da qualsiasi thread vengono sempre indirizzate attraverso il thread dell'Apartment principale per chiamare **DllCanUnloadNow**.

Analogamente ad altri server, i server in-process possono essere a thread singolo, a thread apartment o a thread libero. Questi server possono essere utilizzati da qualsiasi client OLE, indipendentemente dal modello di threading utilizzato da tale client.

Sono consentite tutte le combinazioni di interoperabilità del modello di threading tra client e oggetti in-process. L'interazione tra un client e un oggetto in-process che utilizza modelli di threading diversi è esattamente come l'interazione tra client e server out-of-process. Per un server in-process, quando il modello di threading del client e del server in-process è diverso, è necessario che COM intervenga tra il client e l'oggetto.

Quando un oggetto in-process che supporta il modello a thread singolo viene chiamato simultaneamente da più thread di un client, COM non può consentire ai thread client di accedere direttamente al interfaceâ dell'oggetto. l'oggetto non è stato progettato per tale accesso. COM deve invece garantire che le chiamate siano sincronizzate e vengano effettuate solo dal thread client che ha creato l'oggetto. Quindi, COM crea l'oggetto nell'Apartment principale del client e richiede che tutti gli altri appartamenti client accedano all'oggetto tramite proxy.

Quando un Apartment a thread libero (modello di Apartment a thread multipli) in un client crea un server in-process con threading di tipo Apartment, COM avvia un thread "host" del modello a thread singolo nel client. Questo thread host creerà l'oggetto e verrà eseguito il marshalling del puntatore di interfaccia all'Apartment a thread libero del client. Analogamente, quando un Apartment a thread singolo in un client modello di Apartment crea un server in-process a thread libero, COM avvia un thread host a thread libero (Apartment multithread in cui l'oggetto verrà creato e di cui viene eseguito il marshalling all'Apartment a thread singolo client).

> [!Note]  
> In generale, se si progetta un'interfaccia personalizzata in un server in-process, è necessario fornire anche il codice di marshalling in modo che COM possa effettuare il marshalling dell'interfaccia tra Apartment client.

 

COM consente di proteggere l'accesso agli oggetti forniti da una DLL a thread singolo richiedendo l'accesso dallo stesso Apartment client in cui sono stati creati. Inoltre, tutti i punti di ingresso della DLL, ad esempio [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) e [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow), e i dati globali devono essere sempre accessibili dallo stesso Apartment. COM crea tali oggetti nell'Apartment principale del client, concedendo all'Apartment principale l'accesso diretto ai puntatori dell'oggetto. Le chiamate dagli altri appartamenti usano il marshalling di interthreading per passare dal proxy allo stub nell'Apartment principale e quindi all'oggetto. Ciò consente a COM di sincronizzare le chiamate all'oggetto. Le chiamate interthreading sono lente, quindi è consigliabile riscrivere questi server per supportare più Apartment.

Analogamente a un server in-process a thread singolo, è necessario che venga eseguito l'accesso a un oggetto fornito da una DLL del modello Apartment dallo stesso Apartment client da cui è stato creato. Tuttavia, gli oggetti forniti da questo server possono essere creati in più Apartment del client, quindi il server deve implementare i relativi punti di ingresso (ad esempio [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) e [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)) per l'uso multithread. Se, ad esempio, due Apartment di un client tentano di creare contemporaneamente due istanze dell'oggetto in-process, è possibile chiamare **DllGetClassObject** contemporaneamente da entrambi gli Apartment. È necessario scrivere **DllCanUnloadNow** in modo che la dll non venga scaricata mentre il codice è ancora in esecuzione nella dll.

Se la DLL fornisce solo un'istanza del class factory per creare tutti gli oggetti, l'implementazione di class factory deve essere progettata anche per l'uso multithreading, perché sarà accessibile da più Apartment client. Se la DLL crea una nuova istanza del class factory ogni volta che viene chiamato [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) , il class factory non deve essere thread-safe.

Gli oggetti creati dal class factory non devono essere thread-safe. Una volta creata da un thread, viene sempre eseguito l'accesso all'oggetto tramite tale thread e tutte le chiamate all'oggetto vengono sincronizzate da COM. L'Apartment del modello di Apartment di un client che crea questo oggetto otterrà un puntatore diretto all'oggetto. Gli appartamenti client diversi dall'Apartment in cui è stato creato l'oggetto devono accedere all'oggetto tramite proxy. Questi proxy vengono creati quando il client esegue il marshalling dell'interfaccia tra gli appartamenti.

Quando un valore **ThreadingModel** della dll in-process è impostato su "both", un oggetto fornito da questa dll può essere creato e usato direttamente (senza un proxy) negli Apartment client a thread singolo o multithreading. Tuttavia, può essere utilizzato direttamente solo nell'Apartment in cui è stato creato. Per assegnare l'oggetto a qualsiasi altro Apartment, è necessario effettuare il marshalling dell'oggetto. L'oggetto DLL deve implementare una sincronizzazione personalizzata ed è possibile accedervi da più Apartment client nello stesso momento.

Per velocizzare le prestazioni per l'accesso a thread libero a oggetti DLL in-process, COM fornisce la funzione [**CoCreateFreeThreadedMarshaler**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) . Questa funzione crea un oggetto di marshalling a thread libero che può essere aggregato con un oggetto server in-process. Quando un Apartment client nello stesso processo richiede l'accesso a un oggetto in un altro Apartment, l'aggregazione del gestore di marshalling a thread libero fornisce al client un puntatore diretto all'oggetto server, anziché a un proxy, quando il client esegue il marshalling dell'interfaccia dell'oggetto in un apartment diverso. Il client non deve eseguire alcuna sincronizzazione. Funziona solo all'interno dello stesso processo. il marshalling standard viene usato per un riferimento all'oggetto inviato a un altro processo.

Un oggetto fornito da una DLL in-process che supporta solo il threading libero è un oggetto a thread libero. Implementa la propria sincronizzazione ed è possibile accedervi contemporaneamente da più thread client. Questo server non esegue il marshalling delle interfacce tra thread, quindi questo server può essere creato e usato direttamente (senza proxy) solo da Apartment con multithreading in un client. Gli Apartment a thread singolo che li creano accederanno tramite un proxy.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alle interfacce tra gli Apartment](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Scelta del modello di threading](choosing-the-threading-model.md)
</dt> <dt>

[Apartment con multithreading](multithreaded-apartments.md)
</dt> <dt>

[Processi, thread e Apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicazione a thread singolo e multithreading](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartment a thread singolo](single-threaded-apartments.md)
</dt> </dl>

 

 