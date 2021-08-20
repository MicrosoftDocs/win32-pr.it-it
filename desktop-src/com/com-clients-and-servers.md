---
title: Client e server COM
description: Un aspetto critico di COM è l'interazione tra client e server.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d189b464c8e3a32ff378951067275ab29f5fbabc0b2777c2b2226d632a8bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048659"
---
# <a name="com-clients-and-servers"></a>Client e server COM

Un aspetto critico di COM è l'interazione tra client e server. Un *client COM* è qualsiasi codice o oggetto ottiene un puntatore a un server COM e usa i relativi servizi chiamando i metodi delle relative interfacce. Un *server COM* è qualsiasi oggetto che fornisce servizi ai client. questi servizi sono sotto forma di implementazioni dell'interfaccia COM che possono essere chiamate da qualsiasi client in grado di ottenere un puntatore a una delle interfacce nell'oggetto server.

Esistono due tipi principali di server, *in-process* e *out-of-process.* I server in-process vengono implementati in una libreria collegata dinamica (DLL) e i server out-of-process vengono implementati in un file eseguibile (EXE). I server out-of-process possono risiedere nel computer locale o in un computer remoto. COM fornisce inoltre un meccanismo che consente l'esecuzione di un server in-process (una DLL) in un processo EXE surrogato per sfruttare il vantaggio di poter eseguire il processo in un computer remoto. Per altre informazioni, vedere [Surrogati DLL](dll-surrogates.md).

Il modello di programmazione COM e i costrutti sono stati estesi in modo che i client e i server COM possano lavorare insieme in rete, non solo all'interno di un determinato computer. In questo modo le applicazioni esistenti possono interagire con le nuove applicazioni e tra loro tra reti con un'amministrazione appropriata e le nuove applicazioni possono essere scritte per sfruttare le funzionalità di rete.

Non è necessario che le applicazioni client COM siano consapevoli del modo in cui gli oggetti server vengono pacchetti, indipendentemente dal fatto che siano in pacchetto come oggetti in-process (nelle DLL) o come oggetti locali o remoti (in ESE). Distributed COM consente inoltre di creare pacchetti di oggetti come applicazioni di servizio, sincronizzando COM con le avanzate funzionalità amministrative e di integrazione di sistema di Windows.

> [!Note]  
> In questa documentazione viene usato l'acronimo COM in preferenza per DCOM. Ciò è dovuto al fatto che DCOM non è separato, ma solo COM con una connessione più lunga. Nei casi in cui ciò che viene descritto è in particolare un'operazione remota, viene usato il termine *COM* distribuito.

 

COM è progettato per consentire di aggiungere il supporto per la trasparenza della posizione che si estende in una rete. Consente l'esecuzione di applicazioni scritte per singoli computer in una rete e offre funzionalità che estendono queste funzionalità e aggiungono alla sicurezza necessaria in una rete. Per altre informazioni, vedere [Sicurezza in COM.](security-in-com.md)

COM specifica un meccanismo tramite il quale il codice della classe può essere usato da molte applicazioni diverse.

Per altre informazioni, vedere i seguenti argomenti:

-   [Recupero di un puntatore a un oggetto](getting-a-pointer-to-an-object.md)
-   [Creazione di un oggetto tramite un oggetto classe](creating-an-object-through-a-class-object.md)
-   [Responsabilità del server COM](com-server-responsibilities.md)
-   [Stato dell'oggetto persistente](persistent-object-state.md)
-   [Fornire informazioni sulla classe](providing-class-information.md)
-   [Comunicazione tra oggetti](inter-object-communication.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sincronizzazione delle chiamate](call-synchronization.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




