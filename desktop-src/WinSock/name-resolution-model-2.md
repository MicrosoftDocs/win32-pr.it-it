---
description: Uno spazio dei nomi fa riferimento ad alcune funzionalità per associare (come minimo) il protocollo e gli attributi di indirizzamento di un servizio di rete a uno o più nomi descrittivi.
ms.assetid: 4139a8c2-d940-41e0-a3e8-fce3b70a1ff3
title: Modello di risoluzione dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23395cc6db5a93ec572f59e0d5ac6aaa7890c5c42a7966b86601eb190a54796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822783"
---
# <a name="name-resolution-model"></a>Modello di risoluzione dei nomi

Uno *spazio* dei nomi fa riferimento ad alcune funzionalità per associare (come minimo) il protocollo e gli attributi di indirizzamento di un servizio di rete a uno o più nomi descrittivi. Molti spazi dei nomi sono attualmente in uso a livello ampio, tra cui internet [Domain Name System](../dns/dns-start-page.md) (DNS), [Active Directory Domain Services](../ad/active-directory-domain-services.md), bindery, NetWare Directory Services (NDS) da Novell e X.500. Questi spazi dei nomi variano notevolmente nel modo in cui sono organizzati e implementati. Alcune delle proprietà sono particolarmente importanti da comprendere dal punto di vista della risoluzione dei nomi Winsock.

## <a name="types-of-namespaces"></a>Tipi di spazi dei nomi

Esistono tre diversi tipi di spazi dei nomi in cui è possibile registrare un servizio:

-   Dynamic
-   Static
-   Persistente

Gli spazi dei nomi dinamici consentono ai servizi di registrarsi con lo spazio dei nomi in tempo reale e ai client di individuare i servizi disponibili in fase di esecuzione. Gli spazi dei nomi dinamici si basano spesso sulle trasmissioni per indicare la disponibilità continua di un servizio di rete. Esempi precedenti di spazi dei nomi dinamici includono lo spazio dei nomi Service Advertising Protocol (SAP) usato all'interno di un ambiente NetWare e lo spazio dei nomi NBP (Name Binding Protocol) usato da AppleTalk. Lo spazio dei nomi Peer Name Resolution Protocol (PNRP) usato Windows è un esempio più recente di uno spazio dei nomi dinamico.

Gli spazi dei nomi statici richiedono che tutti i servizi siano registrati in anticipo, ad esempio quando viene creato lo spazio dei nomi. Un esempio di spazio dei nomi statico sono i *file hosts,* *protocol* e *services* usati dalla maggior parte delle implementazioni TCP/IP. In Windows, questi file si trovano in genere nella *cartella C: \\ driver \\ system32 \\ \\* di Windows e così via.

Gli spazi dei nomi persistenti consentono ai servizi di registrarsi con lo spazio dei nomi in tempo reale. A differenza degli spazi dei nomi dinamici, tuttavia, gli spazi dei nomi persistenti mantengono le informazioni di registrazione nell'archiviazione non volatile in cui rimangono fino a quando il servizio non richiede la rimozione. Gli spazi dei nomi persistenti sono tipiizzati dai servizi directory, ad esempio X.500 e NDS (NetWare Directory Service). Questi ambienti consentono l'aggiunta, l'eliminazione e la modifica delle proprietà del servizio. Inoltre, l'oggetto servizio che rappresenta il servizio all'interno del servizio directory potrebbe avere un'ampia gamma di attributi associati al servizio. L'attributo più importante per le applicazioni client è l'indirizzamento delle informazioni del servizio. DNS è un altro esempio di spazio dei nomi permanente. Anche se esiste un modo a livello di codice per risolvere i nomi DNS usando Windows Sockets, il provider dello spazio dei nomi DNS in Windows non supporta la registrazione di nuovi nomi DNS tramite Winsock. È necessario usare direttamente le funzioni DNS per registrare i nomi DNS. Per altre informazioni, vedere Dns [Reference](../dns/dns-reference.md).

## <a name="namespace-organization"></a>Organizzazione dello spazio dei nomi

Molti spazi dei nomi sono disposti gerarchicamente. Alcuni, ad esempio X.500 e NDS, consentono l'annidamento illimitato. Altri consentono di combinare i servizi in un singolo livello di gerarchia o gruppo. Questa operazione viene in genere definita gruppo *di lavoro*. Quando si crea una query, spesso è necessario stabilire un punto di contesto all'interno di una gerarchia dello spazio dei nomi da cui inizierà la ricerca.

## <a name="namespace-provider-architecture"></a>Architettura del provider dello spazio dei nomi

Naturalmente, le interfacce a livello di codice usate per eseguire query sui vari tipi di spazi dei nomi e per registrare le informazioni all'interno di uno spazio dei nomi (se supportato) differiscono notevolmente. Un *provider dello* spazio dei nomi è un software residente in locale che sa come eseguire il mapping tra lo spazio dei nomi SPI di Winsock e uno spazio dei nomi esistente (che può essere implementato in locale o accessibile tramite la rete). L'architettura del provider dello spazio dei nomi è illustrata di seguito:

![Architettura del provider dello spazio dei nomi](images/ovrvw3-1.png)

Si noti che in un determinato spazio dei nomi, ad esempio DNS, è possibile che in un determinato computer siano installati più provider di spazi dei nomi.

Come accennato in precedenza, il termine *generico servizio* si riferisce alla metà del server di un'applicazione client/server. In Winsock un servizio è associato *a* una classe di servizio  e ogni istanza di un particolare servizio ha un nome di servizio che deve essere univoco all'interno della classe di servizio. Esempi di classi di servizio includono SERVER FTP, SQL Server, XYZ Corp. Employee Info Server e così via. Come illustrato nell'esempio, alcune classi di servizio sono note, mentre altre sono univoche e specifiche di una particolare applicazione verticale. In entrambi i casi, ogni classe di servizio è rappresentata sia da un nome di classe che da un identificatore di classe. Il nome della classe non deve necessariamente essere univoco, ma l'identificatore di classe deve essere . I GUID (Globally Unique Identifier) vengono usati per rappresentare gli identificatori di classe del servizio. Per i servizi noti, i nomi di classe e gli identificatori di classe (GUID) sono stati preallocati e sono disponibili macro per la conversione tra, ad esempio, i numeri di porta TCP (in ordine di byte host) e i GUID degli identificatori di classe corrispondenti. Per altri servizi, lo sviluppatore sceglie il nome della classe e usa l'utilità Uuidgen.exe per generare un GUID per l'identificatore di classe.

La nozione di classe di servizio esiste per consentire la definizione di un set di attributi che vengono mantenuti in comune da tutte le istanze di un particolare servizio. Questo set di attributi viene fornito nel momento in cui la classe del servizio è definita in Winsock e viene definita informazioni sullo schema della classe di servizio. Quando un servizio viene installato e reso disponibile in un computer host, tale servizio viene considerato di cui viene creata un'istanza e il relativo nome del servizio viene usato per distinguere una particolare istanza del servizio da altre istanze note allo spazio dei nomi .

Si noti che l'installazione di una classe di servizio deve essere eseguita solo nei computer in cui viene eseguito il servizio, non in tutti i client che possono utilizzare il servizio. Laddove possibile, il32.dll Ws2 fornisce informazioni sullo schema della classe di servizio a un provider dello spazio dei nomi nel momento in cui deve essere registrata un'istanza di un servizio o viene avviata una \_ query del servizio. Il32.dll Ws2, naturalmente, non archivia queste informazioni, ma tenta di recuperarlo da un provider dello spazio dei nomi che ha indicato la possibilità di fornire \_ questi dati. Poiché non esiste alcuna garanzia che il32.dll Ws2 possa fornire lo schema della classe del servizio, i provider dello spazio dei nomi che necessitano di queste informazioni devono avere un meccanismo di fallback per ottenerlo tramite mezzi specifici dello spazio dei \_ nomi.

Come indicato in precedenza, Internet ha adottato quello che può essere definito un modello di servizio incentrato sull'host. Le applicazioni che devono individuare l'indirizzo di trasporto di un servizio in genere devono prima risolvere l'indirizzo di un host specifico noto per ospitare il servizio. A questo indirizzo aggiungono il numero di porta noto e quindi creano un indirizzo di trasporto completo. Per facilitare la risoluzione dei nomi host, è stato preallocato un identificatore di classe di servizio speciale (**SVCID \_ HOSTNAME**). Una query che specifica **SVCID \_ HOSTNAME** come classe del servizio e specifica un nome host per il nome dell'istanza del servizio restituirà informazioni sull'indirizzo host se la query ha esito positivo.

In Windows Sockets 2, le applicazioni indipendenti dal protocollo devono evitare la necessità di comprendere i dettagli interni di un indirizzo di trasporto. Di conseguenza, la necessità di ottenere prima un indirizzo host e quindi aggiungere nella porta è problematica. Per evitare questo problema, le query possono includere anche il nome noto di un particolare servizio e il protocollo su cui opera il servizio, ad esempio FTP su TCP. In questo caso, una query riuscita restituisce un indirizzo di trasporto completo per il servizio specificato nell'host indicato e l'applicazione non è necessaria per controllare gli elementi interni di una struttura [**sockaddr.**](sockaddr-2.md)

Il servizio Internet Domain Name System non dispone di un mezzo ben definito per archiviare le informazioni sullo schema della classe di servizio. Di conseguenza, i provider dello spazio dei nomi DNS per Winsock possono ospitare solo servizi TCP/IP noti per i quali è stato preallocato un GUID di classe di servizio.

In pratica, questa non è una limitazione grave perché i GUID delle classi di servizio sono stati preallocati per l'intero set di porte TCP e UDP e sono disponibili macro per recuperare il GUID associato a qualsiasi porta TCP o UDP con la porta espressa in ordine di byte host. Di conseguenza, tutti i servizi familiari, ad esempio HTTP, FTP, Telnet, Whois e così via, sono ben supportati.

Continuando con l'esempio della classe di servizio, i nomi di istanza del servizio FTP possono essere "alder.intel.com" o "ftp.microsoft.com" mentre un'istanza del server informazioni dipendente XYZ potrebbe essere denominata "XYZ Corp. Employee Info Server versione 3.5".

Nei primi due casi, la combinazione del GUID della classe di servizio per FTP e del nome computer (fornito come nome dell'istanza del servizio) identifica in modo univoco il servizio desiderato. Nel terzo caso, il nome host in cui risiede il servizio può essere individuato in fase di query del servizio, quindi il nome dell'istanza del servizio non deve includere un nome host.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su DNS](../dns/dns-reference.md)
</dt> <dt>

[Strutture dei dati di risoluzione dei nomi](name-resolution-data-structures-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[Riepilogo delle funzioni di risoluzione dei nomi](summary-of-name-resolution-functions-2.md)
</dt> </dl>

 

 
