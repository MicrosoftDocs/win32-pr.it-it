---
title: Spazio di configurazione del dispositivo
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120e12b6480675dba6e735390f4820a8782edc5c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320893"
---
# <a name="device-configuration-space-and-device-configurations"></a>Configurazioni del dispositivo e dello spazio di configurazione del dispositivo

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

*Lo spazio di configurazione* di un dispositivo è il set di tutti i valori possibili che possono essere assegnati a tutti gli attributi del dispositivo. I due motivi più importanti per descrivere lo spazio di configurazione del dispositivo nell'oggetto PrintCapabilities sono i seguenti.

1.  Le informazioni contribuiscono significativamente a una migliore comprensione delle funzionalità del dispositivo. Queste informazioni semplificano la generazione di elementi dell'interfaccia utente da parte di un client di PrintCapabilities, semplificando così la selezione di una particolare configurazione per l'elaborazione di un processo da parte dell'utente finale. Fornendo più dettagli delle funzionalità del dispositivo all'applicazione e infine all'utente finale, l'intenzione di stampa dell'utente può essere soddisfatta in modo più efficace.

2.  Determinate proprietà del dispositivo presentate nell'oggetto PrintCapabilities potrebbero dipendere dalla configurazione specifica selezionata dal client.

Alcune informazioni non devono essere incorporate nell'oggetto PrintCapabilities. Sono incluse le informazioni che non influiscono sulla modalità di creazione di un processo, non impone vincoli sulla modalità di creazione di un processo, né sulle proprietà del dispositivo. Ad esempio, un dispositivo potrebbe essere in grado di segnalare informazioni sullo stato, ad esempio il set di processi in attesa di elaborazione. Queste informazioni non hanno effetto sulle informazioni necessarie per formattare il processo, né forniscono indicazioni sulle funzionalità disponibili nel dispositivo. Per questo motivo, non è necessario che questo tipo di informazioni sia presente nell'oggetto PrintCapabilities.

## <a name="device-constraints"></a>Vincoli del dispositivo

Molti dispositivi non supportano tutte le configurazioni possibili nello spazio di configurazione a causa di un vincolo sul dispositivo. Ad esempio, un dispositivo può essere vincolato dall'esecuzione di stampa duplex su supporti trasparenti. Un vincolo può rappresentare una limitazione fisica: alcuni tipi di supporti sono semplicemente troppo rigidi per spostarsi tra alcuni percorsi di carta nel dispositivo e quindi non possono essere inseriti in alcuni slot di input o essere instradati ad alcuni contenitori di output. Attualmente è responsabilità del provider PrintCapabilities o PrintTicket convalidare la configurazione rappresentata dall'oggetto PrintTicket di input, per verificare che non rappresenti una configurazione non valida. Se la configurazione non è valida, il provider PrintCapabilities o PrintTicket deve modificare la configurazione in modo che diventi valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



