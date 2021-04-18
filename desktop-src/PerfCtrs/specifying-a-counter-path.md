---
description: Il sistema usa i contatori per raccogliere i dati sulle prestazioni.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Specifying a Counter Path (Specifica di un percorso di contatore)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a92f94b4bf3d2252903d92785f43bb0cac110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312084"
---
# <a name="specifying-a-counter-path"></a>Specifying a Counter Path (Specifica di un percorso di contatore)

Il sistema usa i contatori per raccogliere i dati sulle prestazioni. Ogni contatore viene identificato in modo univoco tramite il nome, il percorso o il percorso. La sintassi di un percorso del contatore è:

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

L'elemento computer specifica il nome o l'indirizzo IP del computer da cui si desidera eseguire una query sui dati sulle prestazioni. Il nome del computer è facoltativo se il contatore si trova nel computer locale.

L'elemento PerfObject specifica l'oggetto prestazione su cui eseguire una query. Un oggetto prestazione può essere un componente fisico, ad esempio processori, dischi e memoria, oppure un oggetto di sistema, ad esempio processi e thread. Ogni oggetto di sistema è correlato a un elemento funzionale all'interno del computer ed è associato a un set di contatori standard. Ogni computer potrebbe disporre di un set diverso di oggetti prestazioni e di contatori installati, perché le applicazioni possono installare gli oggetti e i contatori delle prestazioni. Per un elenco degli oggetti e dei contatori delle prestazioni installati nel computer, vedere la finestra di dialogo **Aggiungi contatori** nello strumento prestazioni del computer. Questi oggetti sono elencati anche nella finestra di dialogo PDH Browse (vedere l' [esplorazione dei contatori](browsing-counters.md)). Per un elenco degli oggetti e dei contatori delle prestazioni di sistema, vedere [contatori per oggetto](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).

ParentInstance, ObjectInstance e InstanceIndex sono inclusi nel percorso se possono esistere più istanze dell'oggetto. I processi e i thread, ad esempio, sono più oggetti istanza perché possono essere eseguiti contemporaneamente più processi o thread. Se un oggetto può avere più di un'istanza, è necessario che il percorso del contatore specifichi un'istanza dell'oggetto.

Il formato degli elementi correlati all'istanza dipende dal tipo di oggetto. Se l'oggetto dispone di istanze semplici, il formato è solo il nome dell'istanza racchiuso tra parentesi. Ad esempio:

``` syntax
(Explorer)
```

Se l'istanza di questo oggetto richiede anche un nome di istanza padre, il nome dell'istanza padre deve precedere l'istanza dell'oggetto ed essere separato da un carattere di barra. Ad esempio, i thread appartengono ai processi. Se si esegue una query su un oggetto thread, è necessario specificare anche il processo a cui appartiene, come illustrato nell'esempio seguente:

``` syntax
(Explorer/0)
```

Se l'oggetto dispone di più istanze con la stessa stringa del nome, è possibile indicizzarle in modo sequenziale specificando l'indice dell'istanza preceduto da un segno di cancelletto. Gli indici di istanza sono basati su 0. Se si desidera eseguire una query sulla prima istanza, non includere \# 0, ma è sufficiente specificare il nome dell'istanza. Per specificare la seconda istanza, utilizzare \# 1. per specificare la terza istanza, utilizzare \# 2 e così via. Ad esempio:

``` syntax
(Explorer/0#1)
```

L'elemento contatore specifica il contatore delle prestazioni su cui si desidera eseguire una query per l'oggetto prestazione specificato.

PDH usa i caratteri speciali seguenti in un percorso del contatore. I provider non devono utilizzare questi caratteri nel nome. Se un provider utilizza questi caratteri speciali, PDH non è in grado di analizzare il percorso completo del contatore per ottenere i nomi dei contatori e delle istanze.



| Carattere | Descrizione                                                |
|-----------|------------------------------------------------------------|
| \\        | Separatore generico per computer, oggetto e contatore.       |
| (         | Inizio del nome dell'istanza.                                |
| )         | Fine del nome dell'istanza.                                   |
| /         | Separa l'istanza e l'istanza padre.                    |
| \#n       | Identifica un'occorrenza specifica di un'istanza con nome uguale. |
| \*        | Carattere jolly.                                        |



 

Negli esempi seguenti vengono illustrati i formati possibili per i percorsi dei contatori:

-   \\\\\\contatore oggetto computer (indice padre/istanza \# ) \\
-   \\\\\\contatore oggetto computer (padre/istanza) \\
-   \\\\\\contatore oggetto computer ( \# Indice istanza) \\
-   \\\\\\contatore oggetto computer (istanza) \\
-   \\\\\\contatore oggetto \\ computer
-   \\contatore oggetto (indice padre/istanza \# ) \\
-   \\contatore oggetto (padre/istanza) \\
-   \\contatore oggetto ( \# Indice istanza) \\
-   \\contatore oggetto (istanza) \\
-   \\\\contatore oggetti

## <a name="using-wildcard-characters"></a>Utilizzo di caratteri jolly

I percorsi dei contatori possono contenere un carattere jolly solo per il nome dell'istanza, come illustrato nell'esempio seguente.

``` syntax
\Process(*)\% Processor Time
```

Per espandere il carattere jolly in un elenco di percorsi dei contatori contenenti le istanze trovate nel computer o nel file di log, chiamare [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).

 

 
