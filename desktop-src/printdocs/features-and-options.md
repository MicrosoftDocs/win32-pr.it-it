---
description: Leggere le funzionalità e le opzioni in un documento PrintCapabilities. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 8084fa15-85e5-4c8d-b585-8c349482a6eb
title: Funzionalità e opzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae6d0918b6237885c2c7240efb0dc0f982b882f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549409"
---
# <a name="features-and-options"></a>Funzionalità e opzioni

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

I costrutti di funzionalità/opzione e parametri vengono usati in un documento PrintCapabilities per rappresentare gli attributi del dispositivo che contribuiscono alla definizione della configurazione del dispositivo. Per un esempio di costrutto Feature/Option, si consideri un dispositivo di stampa in grado di stampare in diverse risoluzioni. L'attributo del dispositivo che definisce la risoluzione può essere rappresentato come un'istanza di funzionalità, con ognuno dei possibili valori di risoluzione dell'output rappresentati come singola istanza Di opzione. Un'istanza option può rappresentare una risoluzione di 300 dpi, un'altra può rappresentare una risoluzione di 600 dpi e così via.

Si noti che lo schema di stampa richiede che l'elenco di istanze Feature, Option e ParameterDef segnalate in ogni documento PrintCapabilities rimanga costante, indipendentemente dalla configurazione. In questo modo le configurazioni e le dipendenze dalle configurazioni possono essere espresse in modo non ambiguo. L'implicazione di questo requisito è che ogni funzionalità e funzionalità secondaria deve avere un'impostazione ben definita, indipendentemente dall'impostazione di qualsiasi altra funzionalità o funzionalità secondaria. Pertanto, ogni funzionalità secondaria deve avere un'opzione equivalente a un'impostazione no-op (disattivata, disabilitata o nessuna), che viene selezionata automaticamente per tutte le sottofeature quando l'utente seleziona l'opzione no-op nella funzionalità padre. Al contrario, quando una delle sottofeature è impostata su un'opzione abilitata, vengono abilitate anche la funzionalità padre e le altre funzionalità secondarie associate. Nel frattempo, il provider PrintTicket deve garantire (durante la convalida PrintTicket) che le impostazioni per tutte le istanze di funzionalità e funzionalità secondarie siano definite, indipendentemente dalla configurazione del dispositivo e che le impostazioni delle sottofeature siano coerenti con le impostazioni della funzionalità padre. Ciò garantisce che al dispositivo non sia assegnato un PrintTicket incoerente in cui alcune sottofeature indicano che, ad esempio, la graffatura è abilitata, ma altre sottofeature indicano che la graffatura è disabilitata.

Si noti che gli autori di PrintCapabilities non sono tenuti a usare le funzionalità di annidamento degli elementi feature. Se preferiscono, possono presentare tutte le istanze di funzionalità in una struttura flat, come elementi di pari livello l'uno dell'altro. Si noti anche che una raccolta annidata di istanze di funzionalità può essere appiattita semplicemente spostando tutte le sottofeature al livello radice. L'unica precauzione da prendere è garantire che gli attributi del nome di queste istanze di funzionalità siano univoci.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



