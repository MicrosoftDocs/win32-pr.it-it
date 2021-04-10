---
description: Le interfacce programmatiche utilizzate per eseguire query sui vari tipi di spazi dei nomi e per registrare le informazioni all'interno di uno spazio dei nomi, se supportate, variano notevolmente.
ms.assetid: 6a037e8d-49f3-4286-929a-8bb64ea0960f
title: Architettura del provider dello spazio dei nomi in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1cb567933cae60f56137eba39845bf27ad8c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226081"
---
# <a name="namespace-provider-architecture-in-the-spi"></a>Architettura del provider dello spazio dei nomi in SPI

Le interfacce programmatiche utilizzate per eseguire query sui vari tipi di spazi dei nomi e per registrare le informazioni all'interno di uno spazio dei nomi, se supportate, variano notevolmente. Un provider dello spazio dei nomi è un'applicazione residente localmente che può essere mappata tra lo spazio dei nomi Windows Sockets SPI e uno spazio dei nomi esistente che può essere implementato localmente o a cui si accede tramite la rete. Come illustrato di seguito:

![diagramma del provider dello spazio dei nomi](images/ovrvw3-1.png)

> [!Note]  
> È possibile che uno spazio dei nomi specifico, ad esempio DNS, disponga di più provider dello spazio dei nomi installati in un determinato computer.

 

Come indicato in precedenza, il termine generico Service indica la metà del server di un'applicazione client/server. In Windows Sockets, un servizio è associato a una classe del servizio e ogni istanza di un determinato servizio ha un nome di servizio che deve essere univoco all'interno della classe del servizio. Esempi di classi di servizio includono server FTP, SQL Server, XYZ Corp. Employee info Server e così via.

Come illustrato nell'esempio, alcune classi di servizio sono note, mentre altre sono univoche e specifiche di una particolare applicazione verticale. In entrambi i casi, ogni classe di servizio è rappresentata sia da un nome di classe che da un identificatore di classe. Il nome della classe non deve necessariamente essere univoco, ma l'identificatore di classe deve essere. Gli identificatori univoci globali (GUID) vengono usati per rappresentare gli ID della classe di servizio. Per i servizi noti, i nomi delle classi e gli identificatori di classe (GUID) sono stati preallocati e le macro sono disponibili per la conversione tra, ad esempio, i numeri di porta TCP e i GUID dell'identificatore di classe corrispondente. Per altri servizi, lo sviluppatore sceglie il nome della classe e usa l'utilità Uuidgen.exe per generare un GUID per l'identificatore di classe.

Il concetto di una classe di servizio esiste per consentire la creazione di un set di attributi che vengono mantenuti in comune da tutte le istanze di un determinato servizio. Questo set di attributi viene fornito a Windows Sockets al momento della definizione della classe del servizio e viene definito informazioni sullo schema della classe di servizio. Il \_32.dll WS2 a sua volta inoltra queste informazioni a tutti i provider dello spazio dei nomi attivi. Quando un'istanza di un servizio viene installata e resa disponibile in un computer host, il nome del servizio viene utilizzato per distinguere questa particolare istanza da altri che potrebbero essere noti allo spazio dei nomi.

Tenere presente che l'installazione di una classe di servizio deve essere eseguita solo sui computer in cui viene eseguito il servizio, non su tutti i client che potrebbero utilizzare il servizio. Quando possibile, il \_32.dll WS2 fornirà informazioni sullo schema della classe di servizio a un provider dello spazio dei nomi nel momento in cui un'istanza di un servizio deve essere registrata o viene avviata una query del servizio. Il32.dll WS2, \_ ovviamente, archivia queste informazioni, ma tenta di recuperarle da un provider dello spazio dei nomi che ha indicato la possibilità di fornire questi dati. Poiché non vi è alcuna garanzia che il \_32.dll WS2 possa fornire lo schema della classe di servizio, i provider dello spazio dei nomi che richiedono queste informazioni devono disporre di un meccanismo di fallback per ottenerlo tramite mezzi specifici dello spazio dei nomi.

Internet Domain Name System non dispone di un metodo ben definito per archiviare le informazioni sullo schema della classe di servizio. Di conseguenza, i provider dello spazio dei nomi DNS saranno in grado di gestire solo i servizi TCP/IP noti per i quali è stato preallocato un GUID della classe di servizio. In pratica, non si tratta di una limitazione grave, perché i GUID della classe Service sono stati preallocati per l'intero set di porte TCP e UDP e le macro sono disponibili per recuperare il GUID associato a qualsiasi porta TCP o UDP. Tutti i servizi noti come FTP, Telnet, Whois e così via sono pertanto ben supportati. Quando si eseguono query per questi servizi, per convenzione il nome host del computer di destinazione è il nome dell'istanza del servizio.

Continuando con l'esempio della classe di servizio, i nomi delle istanze del servizio FTP possono essere "alder.intel.com" o "rhino.microsoft.com", mentre un'istanza del server di informazioni del dipendente XYZ Corp potrebbe essere denominata "XYZ Corp. Employee info Server versione 3,5". Nei primi due casi, la combinazione del GUID della classe di servizio per FTP e il nome del computer, fornito come nome dell'istanza del servizio, identificano in modo univoco il servizio desiderato. Nel terzo caso, il nome host in cui risiede il servizio può essere individuato in fase di query del servizio, pertanto non è necessario che il nome dell'istanza del servizio includa un nome host.

 

 



