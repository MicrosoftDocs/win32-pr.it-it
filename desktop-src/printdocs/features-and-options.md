---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 8084fa15-85e5-4c8d-b585-8c349482a6eb
title: Funzionalità e opzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866cead02021b8d933ca03483e77de832d8d094a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320999"
---
# <a name="features-and-options"></a>Funzionalità e opzioni

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

I costrutti di caratteristiche, opzioni e parametri vengono usati in un documento PrintCapabilities per rappresentare gli attributi del dispositivo che contribuiscono alla definizione della configurazione del dispositivo. Per un esempio di un costrutto di funzionalità/opzione, si consideri un dispositivo di stampa in grado di stampare in diverse risoluzioni. L'attributo Device che definisce la risoluzione può essere rappresentato come un'istanza di funzionalità, con ognuno dei possibili valori di risoluzione dell'output rappresentati come singola istanza dell'opzione. Un'istanza di Option può rappresentare una risoluzione di 300 dpi, un'altra può rappresentare una risoluzione di 600 dpi e così via.

Si noti che per lo schema di stampa è necessario che l'elenco delle istanze feature, Option e ParameterDef segnalate in ogni documento PrintCapabilities debba rimanere costante, indipendentemente dalla configurazione. In questo modo le configurazioni e le dipendenze delle configurazioni possono essere espresse in modo non ambiguo. L'implicazione di questo requisito è che ogni funzionalità e sottofunzionalità deve avere un'impostazione ben definita, indipendentemente dall'impostazione di qualsiasi altra funzionalità o funzionalità. Ogni sottofunzionalità deve pertanto avere un'opzione equivalente a un'impostazione no-op (off, disabled o None), che viene selezionata automaticamente per tutte le sottocaratteristiche quando l'utente seleziona l'opzione no-op nella funzionalità padre. Viceversa, quando una delle funzionalità è impostata su un'opzione abilitata, vengono abilitate anche la funzionalità padre e altre sottofunzionalità associate. Nel frattempo, il provider PrintTicket deve garantire (durante la convalida PrintTicket) che vengono definite le impostazioni per tutte le istanze della funzionalità e della funzionalità, indipendentemente dalla configurazione del dispositivo, e che le impostazioni della funzionalità di sottofunzionalità siano coerenti con le impostazioni della funzionalità padre. Ciò garantisce che al dispositivo non venga assegnato un oggetto PrintTicket incoerente in cui alcune sottofunzionalità indicano che, ad esempio, la graffettatura è abilitata, mentre altre sottofunzionalità indicano che la graffettatura è disabilitata.

Si noti che gli autori PrintCapabilities non devono utilizzare le funzionalità di annidamento degli elementi Feature. Se preferiscono, possono presentare tutte le istanze della funzionalità in una struttura piatta, come elementi di pari livello. Si noti inoltre che è possibile rendere flat una raccolta annidata di istanze di funzionalità semplicemente spostando tutte le sottocaratteristiche fino al livello radice. L'unica precauzione da intraprendere consiste nel verificare che gli attributi del nome di queste istanze della funzionalità siano univoci.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



