---
title: Client e server COM
description: Un aspetto fondamentale di COM è il modo in cui i client e i server interagiscono.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710969"
---
# <a name="com-clients-and-servers"></a>Client e server COM

Un aspetto fondamentale di COM è il modo in cui i client e i server interagiscono. Un *client com* è qualsiasi codice o oggetto che ottiene un puntatore a un server com e utilizza i relativi servizi chiamando i metodi delle relative interfacce. Un *Server com* è qualsiasi oggetto che fornisce servizi ai client; questi servizi sono sotto forma di implementazioni di interfaccia COM che possono essere chiamate da qualsiasi client in grado di ottenere un puntatore a una delle interfacce nell'oggetto server.

Esistono due tipi principali di server, *in-process* e *out-of-process*. I server in-process sono implementati in una libreria a collegamento dinamico (DLL) e i server out-of-process sono implementati in un file eseguibile (EXE). I server out-of-process possono risiedere nel computer locale o in un computer remoto. Inoltre, COM fornisce un meccanismo che consente a un server in-process (DLL) di essere eseguito in un processo di EXE surrogato per ottenere il vantaggio di poter eseguire il processo in un computer remoto. Per ulteriori informazioni, vedere la pagina relativa ai [surrogati dll](dll-surrogates.md).

Il modello di programmazione COM e i costrutti sono ora stati estesi in modo che i client e i server COM possano interagire in rete, non solo all'interno di un determinato computer. In questo modo le applicazioni esistenti possono interagire con le nuove applicazioni e tra loro attraverso le reti con l'amministrazione corretta e le nuove applicazioni possono essere scritte per sfruttare le funzionalità di rete.

Non è necessario che le applicazioni client COM siano consapevoli del modo in cui gli oggetti server sono inclusi nel pacchetto, che siano inclusi in un pacchetto come oggetti in-process (in dll) o come oggetti locali o remoti (in exe). Distributed COM consente inoltre di creare pacchetti di oggetti come applicazioni di servizio, sincronizzando COM con le complesse funzionalità amministrative e di integrazione di sistema di Windows.

> [!Note]  
> In questa documentazione l'acronimo COM viene usato in modo preferenziale per DCOM. Questo perché DCOM non è separato, ma è solo COM con una rete più lunga. Nei casi in cui viene descritto in particolare un'operazione remota, viene usato il termine *Distributed COM* .

 

COM è progettato per consentire di aggiungere il supporto per la trasparenza della località che si estende in una rete. Consente le applicazioni scritte per i singoli computer per l'esecuzione in una rete e fornisce funzionalità che estendono queste funzionalità e aggiungono alla sicurezza necessaria in una rete. Per ulteriori informazioni, vedere [sicurezza in com](security-in-com.md).

COM specifica un meccanismo mediante il quale il codice della classe può essere utilizzato da molte applicazioni diverse.

Per altre informazioni, vedere i seguenti argomenti:

-   [Recupero di un puntatore a un oggetto](getting-a-pointer-to-an-object.md)
-   [Creazione di un oggetto tramite un oggetto classe](creating-an-object-through-a-class-object.md)
-   [Responsabilità server COM](com-server-responsibilities.md)
-   [Stato oggetto permanente](persistent-object-state.md)
-   [Fornire informazioni sulla classe](providing-class-information.md)
-   [Comunicazione tra oggetti](inter-object-communication.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sincronizzazione delle chiamate](call-synchronization.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




