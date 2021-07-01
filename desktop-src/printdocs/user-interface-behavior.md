---
description: Esaminare una discussione sul comportamento dell'interfaccia utente in relazione alle funzionalità e alle opzioni per documenti e stampa.
ms.assetid: dc19a568-3673-4061-b19a-50d5df0485d0
title: Interfaccia utente comportamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81d007c653ed3f019892e944d9fa4203dc6de11
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119436"
---
# <a name="user-interface-behavior"></a>Interfaccia utente comportamento

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Si supponga di creare un client PrintCapabilities che legge un documento PrintCapabilities e seleziona una o più opzioni da ogni funzionalità e le usa per costruire un PrintTicket che specifica la configurazione da usare per elaborare il processo. Per ogni funzionalità di interesse, il client deve esaminare ogni opzione e decidere se tale opzione è appropriata per l'attività in fase di esecuzione. Per un'opzione senza parametri, può essere valutata accedendo al valore di ogni ScoredProperty. Nel caso di un'opzione di dimensioni dei supporti senza parametri, il client determina se le dimensioni di larghezza e altezza dei supporti segnalati in ogni opzione corrispondono alle dimensioni richieste.

Nel caso dell'opzione con parametri, il client deve accedere all'istanza di ParameterDef indicata nell'istanza ParameterRef contenuta in una delle istanze scoredProperty. ParameterDef definisce in genere l'intervallo di valori consentiti per il parametro , nonché le unità (pollici, mm e così via) rappresentate dal valore . Se le dimensioni richieste rientrano nell'intervallo di valori consentiti per ognuno dei parametri, il client ha l'attività aggiuntiva di inizializzazione dei parametri (tramite un'istanza ParameterInit) in PrintTicket. Si tratta di un'attività particolarmente importante. Ad esempio, un PrintTicket non deve specificare una dimensione del supporto personalizzata senza specificare le dimensioni del supporto, perché l'oggetto PrintTicket risultante sarà ambiguo e non definito.

Se il client è un'interfaccia utente, è necessario gestire un set di circostanze simile. L'interfaccia utente visualizza in genere i valori delle istanze scoredProperty definite per ogni opzione. Per maggiore chiarezza, è essenziale visualizzare l'intervallo e le unità consentiti per i parametri in un'opzione con parametri. Inoltre, se l'utente seleziona l'opzione con parametri, l'interfaccia utente deve richiedere all'utente di immettere il valore da usare per inizializzare ogni parametro. Infine, l'interfaccia utente deve comporre un PrintTicket che rifletta tutte le selezioni dell'utente.

Per informazioni dettagliate sulla costruzione di PrintTicket e sulla specifica dell'inizializzazione dei parametri, vedere Creazione di [un Device-Specific PrintTicket.](creating-a-device-specific-printticket.md) Per informazioni sulla dereferenziazione di istanze ParameterRef e sull'interpretazione delle istanze ParameterDef, vedere [Uso di parametri.](using-parameters.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



