---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: dc19a568-3673-4061-b19a-50d5df0485d0
title: Comportamento dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d475472330c8e3ba2ceb06d0cbde9f3a7fb0be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320986"
---
# <a name="user-interface-behavior"></a>Comportamento dell'interfaccia utente

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Si supponga di creare un client PrintCapabilities che legga in un documento PrintCapabilities e selezioni una o più opzioni da ogni funzionalità e le usi per costruire un oggetto PrintTicket che specifichi la configurazione da usare per elaborare il processo. Per ogni funzionalità di interesse, il client deve esaminare ogni opzione e decidere se questa opzione è appropriata per l'attività. Per un'opzione che non è parametrizzata, può essere valutata accedendo al valore di ogni ScoredProperty. Nel caso di un'opzione di dimensione media non parametrizzata, il client determina se le dimensioni della larghezza e dell'altezza del supporto segnalato in ogni opzione corrispondono alle dimensioni richieste.

Nel caso dell'opzione con parametri, il client deve accedere all'istanza di ParameterDef indicata nell'istanza di ParameterRef contenuta in una delle istanze di ScoredProperty. ParameterDef in genere definisce l'intervallo di valori consentito per il parametro, nonché le unità (pollici, mm e così via) rappresentate dal valore. Se le dimensioni necessarie rientrano nell'intervallo di valori consentito per ognuno dei parametri, il client ha l'attività aggiuntiva di inizializzazione dei parametri (mediante un'istanza di ParameterInit) nell'oggetto PrintTicket. Si tratta di un'attività particolarmente importante. Un oggetto PrintTicket, ad esempio, non deve specificare una dimensione del supporto personalizzata senza specificare le dimensioni del supporto, perché l'oggetto PrintTicket risultante sarà ambiguo e non è definito in modo corretto.

Se il client è un'interfaccia utente, è necessario gestire un set di circostanze analogo. L'interfaccia utente visualizza in genere i valori delle istanze di ScoredProperty definite per ogni opzione. Per maggiore chiarezza, è essenziale visualizzare l'intervallo e le unità consentiti per i parametri in un'opzione con parametri. Inoltre, se l'utente seleziona l'opzione con parametri, l'interfaccia utente (UI) deve richiedere all'utente di immettere il valore da usare per inizializzare ogni parametro. Infine, l'interfaccia utente deve comporre un oggetto PrintTicket che rifletta tutte le selezioni dell'utente.

Per informazioni dettagliate sulla costruzione e la specifica dell'inizializzazione dei parametri, vedere [creazione di un Device-Specific PrintTicket](creating-a-device-specific-printticket.md). Per informazioni su come dereferenziare le istanze di ParameterRef e interpretare le istanze di ParameterDef, vedere [uso dei parametri](using-parameters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



