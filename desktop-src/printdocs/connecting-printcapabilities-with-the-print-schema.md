---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 2f6c51a3-003c-4d68-9e4d-9be5d325a477
title: Connessione di PrintCapabilities con lo schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2f5a34421dba2402bce1d6699f208fd58c799
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321058"
---
# <a name="connecting-printcapabilities-with-the-print-schema"></a>Connessione di PrintCapabilities con lo schema di stampa

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema PrintCapabilities generale copre la struttura, lo scopo e l'utilizzo dei diversi tipi di elementi. Specifica l'attributo del nome usato per definire istanze specifiche di ogni tipo di elemento. Specifica che gli autori PrintCapabilities possono usare istanze di elementi definiti dalle parole chiave dello schema di stampa oppure possono introdurre istanze personalizzate definite privatamente, purché queste istanze definite privatamente siano definite in uno spazio dei nomi che è chiaramente identificato come loro. Gli autori PrintCapabilities possono inoltre utilizzare istanze definite in precedenza in un altro spazio dei nomi privato.

Il documento parole chiave dello schema di stampa definisce le istanze specifiche di ogni tipo di elemento disponibile per l'utilizzo nei documenti PrintCapabilities e negli PrintTicket. Ne documenta anche lo scopo e l'utilizzo. Il documento parole chiave dello schema di stampa definisce anche le istanze di diversi tipi di elemento, come indicato di seguito:

-   Istanze di proprietà e sottoproprietà che risiedono alla radice del documento PrintCapabilities

    -   Questi elementi descrivono i vari aspetti e funzionalità del dispositivo e forniscono un vocabolario comune per la descrizione dei dispositivi.

-   Istanze di proprietà e sottoproprietà che sono elementi figlio di elementi Feature

    -   Questi elementi descrivono i vari aspetti correlati a una funzionalità specifica.

-   Istanze di proprietà e sottoproprietà figlio di elementi option

    -   Questi elementi descrivono i vari aspetti e le funzionalità del dispositivo che dipendono dall'opzione selezionata per una funzionalità specifica. Questi possono essere sostituiti da istanze di proprietà situate nella radice del documento PrintCapabilities, ma in alcuni casi offrono praticità aggiuntiva. Per ulteriori informazioni, vedere [aggiunta di istanze di proprietà](adding-property-instances.md).

<!-- -->

-   Istanze di ScoredProperty

    -   Le istanze di ScoredProperty definiscono il linguaggio usato per caratterizzare un'opzione. Le istanze di ScoredProperty definite nelle parole chiave dello schema di stampa rendono possibile le istanze di opzioni scritte da molte parti diverse per la portabilità di molti dispositivi e per essere riconosciute da qualsiasi altro driver di dispositivo o provider PrintCapabilities o PrintTicket.

-   Istanze del valore ScoredProperty

    -   Queste istanze di valore vengono fornite per lo stesso motivo per cui vengono fornite le istanze di ScoredProperty.

-   Istanze delle funzionalità

    -   Ogni opzione deve appartenere a una funzionalità specifica, richiedendo in tal modo la definizione della funzionalità stessa.

-   Istanze di ParameterDef

    -   Un'istanza di Print Schema Keywords-fornito ParameterDef definisce anche un valore per ogni proprietà contenuta. Il provider PrintCapabilities è libero di modificare le istanze di valore per le istanze di proprietà che possono essere modificate. Per informazioni sulle istanze di proprietà che è possibile modificare e che non possono essere modificate (non modificabili), vedere [elementi ParameterDef e ParameterInit](parameterdef-and-parameterinit-elements.md).

È importante notare che lo schema PrintCapabilities non assegna alcun nome alle istanze di opzioni. Le istanze delle opzioni sono caratterizzate esclusivamente dalle istanze ScoredProperty rilevate nel loro complesso. Un malinteso comune è che l'uso dell'attributo ' name ' per definire un'opzione consente di identificare le istanze delle opzioni, ma ciò non è corretto. Non è necessario che gli elementi option siano univoci per le istanze di opzioni di pari livello, né utilizzino l'attributo ' name ' per definire un'opzione obbligatoria.

Il documento parole chiave di Print Schema definisce uno spazio dei nomi standard a cui appartengono tutti gli attributi del nome di istanza negli schemi PrintCapabilities e PrintTicket. Tutti i tag del tipo di elemento e gli attributi XML usati dai tipi di elemento appartengono anche a questo spazio dei nomi.

Per ogni istanza definita nello schema PrintCapabilities, lo schema PrintCapabilities specifica sia l'attributo Name che la posizione dell'istanza. Il provider e il client devono mantenere entrambi i casi quando si utilizza questa istanza nel relativo documento PrintCapabilities o PrintTicket.

Il documento parole chiave dello schema di stampa designa alcune istanze come obbligatorie. Queste istanze devono essere visualizzate in ogni documento PrintCapabilities e devono essere inizializzate correttamente con valori validi. Tutte le istanze nelle parole chiave dello schema di stampa che non sono designate come obbligatorie sono facoltative.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



