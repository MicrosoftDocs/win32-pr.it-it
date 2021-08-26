---
title: Spazio di configurazione del dispositivo
description: Lo spazio di configurazione di un dispositivo è il set di tutti i valori possibili che possono essere assegnati a tutti gli attributi del dispositivo.
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09eabf7c84e1990e0aaf6b2d9fab1d9043f788fef32c3863a71d9ca1e6b61a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092116"
---
# <a name="device-configuration-space-and-device-configurations"></a>Spazio di configurazione del dispositivo e configurazioni dei dispositivi

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo spazio di *configurazione di un* dispositivo è il set di tutti i valori possibili che possono essere assegnati a tutti gli attributi del dispositivo. I due motivi più importanti per descrivere lo spazio di configurazione del dispositivo in PrintCapabilities sono i seguenti.

1.  Le informazioni contribuiscono in modo significativo a una maggiore comprensione delle funzionalità del dispositivo. Queste informazioni semplificano la generazione di elementi dell'interfaccia utente (UI) da parte di un client di PrintCapabilities, semplificando la selezione di una configurazione specifica per l'elaborazione di un processo da parte dell'utente finale. Fornendo più dettagli delle funzionalità del dispositivo all'applicazione e infine all'utente finale, la finalità di stampa dell'utente può essere soddisfatta in modo più efficace.

2.  Alcune proprietà del dispositivo presentate in PrintCapabilities potrebbero dipendere dalla configurazione specifica selezionata dal client.

Alcune informazioni non devono essere incorporate in PrintCapabilities. Sono incluse informazioni che non influiscono sulla modalità di creazione di un processo, non impongono vincoli sulla modalità di creazione di un processo né influiscono in altro modo sulle proprietà del dispositivo. Ad esempio, un dispositivo potrebbe essere in grado di segnalare informazioni sullo stato, ad esempio il set di processi in attesa di elaborazione. Queste informazioni non influisce sulle informazioni necessarie per formattare il processo, né forniscono alcuna indicazione delle funzionalità disponibili nel dispositivo. Per questo motivo, questo tipo di informazioni non deve essere presente in PrintCapabilities.

## <a name="device-constraints"></a>Vincoli del dispositivo

Molti dispositivi non supportano tutte le configurazioni possibili nello spazio di configurazione a causa di un vincolo nel dispositivo. Ad esempio, un dispositivo può essere vincolato dall'esecuzione di stampa duplex su supporti trasparenti. Un vincolo può rappresentare una limitazione fisica: alcuni tipi di supporti sono semplicemente troppo rigidi per passare attraverso determinati percorsi cartacei nel dispositivo e quindi non possono essere inseriti in alcuni slot di input o essere indirizzati ad alcuni contenitori di output. Attualmente è responsabilità del provider PrintCapabilities o PrintTicket convalidare la configurazione rappresentata dall'input PrintTicket, per verificare che non rappresenti una configurazione non valida. Se la configurazione non è valida, il provider PrintCapabilities o PrintTicket deve modificare la configurazione in modo che diventi valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



