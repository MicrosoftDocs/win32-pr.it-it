---
description: Il sistema usa i contatori per raccogliere i dati sulle prestazioni.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Specifying a Counter Path (Specifica di un percorso di contatore)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a359762e4d959992bebd338c4b3ee29825c63b4cb081b70722c82fb3376b5d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143804"
---
# <a name="specifying-a-counter-path"></a>Specifying a Counter Path (Specifica di un percorso di contatore)

Il sistema usa i contatori per raccogliere i dati sulle prestazioni. Ogni contatore viene identificato in modo univoco tramite il nome e il percorso o la posizione. La sintassi di un percorso contatore è:

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

L'elemento Computer specifica il nome o l'indirizzo IP del computer da cui si desidera eseguire query sui dati sulle prestazioni. Il nome del computer è facoltativo se il contatore si trova nel computer locale.

L'elemento PerfObject specifica l'oggetto prestazioni su cui eseguire la query. Un oggetto prestazione può essere un componente fisico, ad esempio processori, dischi e memoria, oppure un oggetto di sistema, ad esempio processi e thread. Ogni oggetto di sistema è correlato a un elemento funzionale all'interno del computer e dispone di un set di contatori standard assegnati. In ogni computer può essere installato un set diverso di oggetti prestazioni e contatori perché le applicazioni possono installare i propri oggetti prestazioni e contatori. Per un elenco degli oggetti prestazioni e dei contatori installati nel computer, vedere la finestra di dialogo Aggiungi contatori nello strumento Prestazioni del computer.  Questi oggetti sono elencati anche nella finestra di dialogo sfoglia PDH (vedere [Contatori di esplorazione](browsing-counters.md)). Per un elenco di contatori e oggetti prestazioni di sistema, vedere [Counters by Object](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).

ParentInstance, ObjectInstance e InstanceIndex sono inclusi nel percorso se possono esistere più istanze dell'oggetto. Ad esempio, i processi e i thread sono più oggetti istanza perché più processi o thread possono essere eseguiti contemporaneamente. Se un oggetto può avere più di un'istanza, il percorso del contatore deve specificare un'istanza dell'oggetto.

Il formato degli elementi correlati all'istanza dipende dal tipo di oggetto. Se l'oggetto ha istanze semplici, il formato è solo il nome dell'istanza racchiuso tra parentesi. Esempio:

``` syntax
(Explorer)
```

Se l'istanza di questo oggetto richiede anche un nome di istanza padre, il nome dell'istanza padre deve essere prima dell'istanza dell'oggetto ed essere separato da una barra. Ad esempio, i thread appartengono ai processi. Se si esegue una query su un oggetto thread, è necessario specificare anche il processo a cui appartiene, come illustrato nell'esempio seguente:

``` syntax
(Explorer/0)
```

Se l'oggetto dispone di più istanze che hanno la stessa stringa del nome, possono essere indicizzate in sequenza specificando l'indice dell'istanza preceduto da un simbolo di cancelletto. Gli indici dell'istanza sono in base 0. Se si vuole eseguire una query sulla prima istanza, non includere \# 0, ma specificare solo il nome dell'istanza. Per specificare la seconda istanza, \# usare 1; per specificare la terza istanza, \# usare 2 e così via. Esempio:

``` syntax
(Explorer/0#1)
```

L'elemento Counter specifica il contatore delle prestazioni su cui eseguire una query per l'oggetto prestazioni specificato.

PDH usa i caratteri speciali seguenti in un percorso contatore. I provider non devono usare questi caratteri nei nomi. Se un provider utilizza questi caratteri speciali, PDH non può analizzare il percorso completo del contatore per ottenere i nomi dei contatori e delle istanze.



| Carattere | Descrizione                                                |
|-----------|------------------------------------------------------------|
| \\        | Separatore generico per computer, oggetto e contatore.       |
| (         | Inizio del nome dell'istanza.                                |
| )         | Fine del nome dell'istanza.                                   |
| /         | Separa l'istanza e l'istanza padre.                    |
| \#n       | Identifica un'occorrenza specifica di un'istanza con lo stesso nome. |
| \*        | Carattere jolly.                                        |



 

Gli esempi seguenti illustrano i formati possibili per i percorsi dei contatori:

-   \\\\contatore \\ computer object(parent/instance \# \\ index)
-   \\\\contatore \\ oggetto computer (padre/istanza) \\
-   \\\\contatore \\ dell'oggetto computer \# (indice \\ dell'istanza)
-   \\\\contatore \\ oggetto computer \\ (istanza)
-   \\\\contatore \\ dell'oggetto \\ computer
-   \\contatore object(parent/instance \# \\ index)
-   \\Contatore \\ object(parent/instance)
-   \\contatore object(instance \# \\ index)
-   \\contatore object(instance) \\
-   \\contatore \\ oggetti

## <a name="using-wildcard-characters"></a>Uso di caratteri jolly

I percorsi dei contatori possono contenere un carattere jolly solo per il nome dell'istanza, come illustrato nell'esempio seguente.

``` syntax
\Process(*)\% Processor Time
```

Per espandere il carattere jolly in un elenco di percorsi dei contatori che contengono istanze trovate nel computer o nel file di log, chiamare [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).

 

 
