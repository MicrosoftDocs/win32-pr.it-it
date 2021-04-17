---
description: Uno spazio dei nomi si riferisce a una funzionalità che consente di associare (come minimo) il protocollo e gli attributi di indirizzamento di un servizio di rete con uno o più nomi descrittivi.
ms.assetid: 4139a8c2-d940-41e0-a3e8-fce3b70a1ff3
title: Modello di risoluzione dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb209254dcee2419e1ed92c017fc7d37dc9c0a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526149"
---
# <a name="name-resolution-model"></a>Modello di risoluzione dei nomi

Uno *spazio dei nomi* si riferisce a una funzionalità che consente di associare (come minimo) il protocollo e gli attributi di indirizzamento di un servizio di rete con uno o più nomi descrittivi. Molti spazi dei nomi sono attualmente in uso, tra cui Internet [Domain Name System](../dns/dns-start-page.md) (DNS), [Active Directory Domain Services](../ad/active-directory-domain-services.md), bindery, servizi directory NetWare (NDS) da Novell e X. 500. Questi spazi dei nomi variano notevolmente nel modo in cui sono organizzati e implementati. Alcune proprietà sono particolarmente importanti da comprendere dal punto di vista della risoluzione dei nomi Winsock.

## <a name="types-of-namespaces"></a>Tipi di spazi dei nomi

Sono disponibili tre tipi diversi di spazi dei nomi in cui è possibile registrare un servizio:

-   Dynamic
-   Static
-   Persistente

Gli spazi dei nomi dinamici consentono ai servizi di registrarsi allo spazio dei nomi in tempo reale e ai client di individuare i servizi disponibili in fase di esecuzione. Gli spazi dei nomi dinamici si basano spesso sulle trasmissioni per indicare la disponibilità continua di un servizio di rete. Esempi meno recenti di spazi dei nomi dinamici includono lo spazio dei nomi Service Advertising Protocol (SAP) utilizzato in un ambiente NetWare e lo spazio dei nomi avvio (name binding Protocol) utilizzato da AppleTalk. Lo spazio dei nomi del protocollo PNRP (Peer Name Resolution Protocol) usato in Windows è un esempio più recente di uno spazio dei nomi dinamico.

Gli spazi dei nomi statici richiedono la registrazione di tutti i servizi in anticipo, ovvero quando viene creato lo spazio dei nomi. Un esempio di uno spazio dei nomi statico è costituito dai file *host*, *protocollo* e *Servizi* utilizzati dalla maggior parte delle implementazioni TCP/IP. In Windows, questi file si trovano in genere nella cartella *C: \\ Windows \\ system32 \\ drivers e \\ così via* .

Gli spazi dei nomi permanenti consentono ai servizi di eseguire la registrazione con lo spazio dei nomi in tempo reale. A differenza degli spazi dei nomi dinamici, tuttavia, gli spazi dei nomi persistenti conservano le informazioni di registrazione in una risorsa di archiviazione non volatile dove rimangono fino al momento in cui il servizio richiede la rimozione. Gli spazi dei nomi permanenti sono caratterizzati da servizi directory quali X. 500 e NDS (servizio directory NetWare). Questi ambienti consentono l'aggiunta, l'eliminazione e la modifica delle proprietà del servizio. Inoltre, l'oggetto servizio che rappresenta il servizio all'interno del servizio directory potrebbe avere un'ampia gamma di attributi associati al servizio. L'attributo più importante per le applicazioni client è le informazioni di indirizzamento del servizio. DNS è un altro esempio di uno spazio dei nomi persistente. Sebbene esista un metodo programmatico per risolvere i nomi DNS con Windows Sockets, il provider dello spazio dei nomi DNS in Windows non supporta la registrazione di nuovi nomi DNS con Winsock. È necessario usare direttamente le funzioni DNS per registrare i nomi DNS. Per ulteriori informazioni, vedere il [riferimento DNS](../dns/dns-reference.md).

## <a name="namespace-organization"></a>Organizzazione dello spazio dei nomi

Molti spazi dei nomi sono disposti gerarchicamente. Alcuni, ad esempio X. 500 e NDS, consentono l'annidamento illimitato. Altri consentono di combinare i servizi in un singolo livello di gerarchia o gruppo. Questa operazione viene in genere definita *gruppo* di lavoro. Quando si crea una query, spesso è necessario stabilire un punto di contesto all'interno di una gerarchia dello spazio dei nomi da cui inizierà la ricerca.

## <a name="namespace-provider-architecture"></a>Architettura del provider dello spazio dei nomi

Naturalmente, le interfacce programmatiche utilizzate per eseguire query sui vari tipi di spazi dei nomi e per registrare le informazioni all'interno di uno spazio dei nomi (se supportato) variano notevolmente. Un *provider dello spazio dei nomi* è un componente software residente localmente che sa come eseguire il mapping tra lo spazio dei nomi di Winsock e uno spazio dei nomi esistente, che può essere implementato localmente o accessibile tramite la rete. L'architettura del provider dello spazio dei nomi è illustrata di seguito:

![architettura del provider dello spazio dei nomi](images/ovrvw3-1.png)

Si noti che è possibile che per uno spazio dei nomi specifico venga installato più di un provider dello spazio dei nomi in un determinato computer.

Come indicato in precedenza, il termine generico *servizio* fa riferimento alla metà del server di un'applicazione client/server. In Winsock un servizio è associato a una *classe del servizio* e ogni istanza di un determinato servizio ha un *nome di servizio* che deve essere univoco all'interno della classe del servizio. Esempi di classi di servizio includono server FTP, SQL Server, XYZ Corp. Employee info Server e così via. Come illustrato nell'esempio, alcune classi di servizio sono note, mentre altre sono univoche e specifiche di una particolare applicazione verticale. In entrambi i casi, ogni classe di servizio è rappresentata sia da un nome di classe che da un identificatore di classe. Il nome della classe non deve necessariamente essere univoco, ma l'identificatore di classe deve essere. Gli identificatori univoci globali (GUID) vengono usati per rappresentare gli identificatori delle classi di servizio. Per i servizi noti, i nomi delle classi e gli identificatori di classe (GUID) sono stati preallocati e le macro sono disponibili per la conversione tra, ad esempio, i numeri di porta TCP (nell'ordine dei byte host) e i GUID dell'identificatore di classe corrispondente. Per altri servizi, lo sviluppatore sceglie il nome della classe e usa l'utilità Uuidgen.exe per generare un GUID per l'identificatore di classe.

La nozione di classe del servizio esiste per consentire di stabilire un set di attributi che vengono mantenuti in comune da tutte le istanze di un determinato servizio. Questo set di attributi viene fornito nel momento in cui la classe del servizio viene definita in Winsock ed è denominata informazioni sullo schema della classe di servizio. Quando un servizio viene installato e reso disponibile in un computer host, tale servizio viene considerato di cui viene *creata un'istanza* e viene usato il nome del servizio per distinguere una particolare istanza del servizio da altre istanze che potrebbero essere note allo spazio dei nomi.

Si noti che l'installazione di una classe di servizio deve essere eseguita solo sui computer in cui viene eseguito il servizio, non su tutti i client che potrebbero utilizzare il servizio. Laddove possibile, il \_32.dll WS2 fornisce informazioni sullo schema della classe di servizio a un provider dello spazio dei nomi nel momento in cui deve essere registrata la creazione di un'istanza di un servizio o se viene avviata una query del servizio. Il32.dll WS2, \_ ovviamente, archivia queste informazioni, ma tenta di recuperarle da un provider dello spazio dei nomi che ha indicato la possibilità di fornire questi dati. Poiché non vi è alcuna garanzia che il \_32.dll WS2 possa fornire lo schema della classe di servizio, i provider dello spazio dei nomi che necessitano di queste informazioni devono disporre di un meccanismo di fallback per ottenerlo tramite mezzi specifici dello spazio dei nomi.

Come indicato in precedenza, Internet ha adottato la definizione di un modello di servizio incentrato sull'host. Le applicazioni che necessitano di individuare l'indirizzo di trasporto di un servizio in genere devono innanzitutto risolvere l'indirizzo di un host specifico noto per ospitare il servizio. A questo indirizzo vengono aggiunti nel numero di porta noto e pertanto viene creato un indirizzo di trasporto completo. Per semplificare la risoluzione dei nomi host, un identificatore di classe di servizio speciale è stato preallocato (**SVCID \_ hostname**). Una query che specifica il nome host **SVCID \_** come classe del servizio e specifica un nome host per il nome dell'istanza del servizio restituirà informazioni sull'indirizzo host se la query ha esito positivo.

In Windows Sockets 2, le applicazioni indipendenti dal protocollo devono evitare la necessità di comprendere i dettagli interni di un indirizzo di trasporto. Quindi, la necessità di ottenere prima un indirizzo host e quindi aggiungere la porta è problematica. Per evitare questo problema, le query possono includere anche il nome noto di un determinato servizio e il protocollo su cui opera il servizio, ad esempio FTP su TCP. In questo caso, una query con esito positivo restituisce un indirizzo di trasporto completo per il servizio specificato nell'host indicato e non è necessario che l'applicazione controlli gli elementi interni di una struttura [**sockaddr**](sockaddr-2.md) .

Il Domain Name System di Internet non dispone di un metodo ben definito per archiviare le informazioni sullo schema della classe di servizio. Di conseguenza, i provider dello spazio dei nomi DNS per Winsock possono ospitare solo servizi TCP/IP noti per i quali è stato preallocato un GUID della classe di servizio.

In pratica, non si tratta di una limitazione grave, perché i GUID della classe di servizio sono stati preallocati per l'intero set di porte TCP e UDP e le macro sono disponibili per recuperare il GUID associato a qualsiasi porta TCP o UDP con la porta espressa nell'ordine dei byte host. Tutti i servizi noti come HTTP, FTP, Telnet, Whois e così via sono pertanto ben supportati.

Continuando con l'esempio della classe di servizio, i nomi delle istanze del servizio FTP possono essere "alder.intel.com" o "ftp.microsoft.com", mentre un'istanza del server di informazioni del dipendente XYZ Corp potrebbe essere denominata "XYZ Corp. Employee info Server versione 3,5".

Nei primi due casi, la combinazione del GUID della classe di servizio per FTP e il nome del computer, fornito come nome dell'istanza del servizio, identificano in modo univoco il servizio desiderato. Nel terzo caso, il nome host in cui risiede il servizio può essere individuato in fase di query del servizio, pertanto non è necessario che il nome dell'istanza del servizio includa un nome host.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento DNS](../dns/dns-reference.md)
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

 

 
