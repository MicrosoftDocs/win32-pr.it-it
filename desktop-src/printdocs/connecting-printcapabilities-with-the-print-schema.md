---
description: Informazioni sullo schema PrintCapabilities generale, che illustra la struttura, lo scopo e l'uso dei vari tipi di elementi.
ms.assetid: 2f6c51a3-003c-4d68-9e4d-9be5d325a477
title: Connessione di PrintCapabilities con lo schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661a8eb93c6f788381713c0c6620e8a09a53648f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409644"
---
# <a name="connecting-printcapabilities-with-the-print-schema"></a>Connessione di PrintCapabilities con lo schema di stampa

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema PrintCapabilities generale illustra la struttura, lo scopo e l'uso dei vari tipi di elementi. Specifica l'attributo name usato per definire istanze specifiche di ogni tipo di elemento. Specifica che gli autori printcapabilities possono usare istanze di elementi definiti dalle parole chiave dello schema di stampa oppure possono introdurre le proprie istanze definite privatamente, purché queste istanze definite privatamente siano definite in uno spazio dei nomi chiaramente identificato come proprie. Gli autori di PrintCapabilities possono anche usare istanze definite in precedenza in un altro spazio dei nomi privato.

Il documento Parole chiave dello schema di stampa definisce le istanze specifiche di ogni tipo di elemento disponibili per l'uso nei documenti PrintCapabilities e in PrintTickets. Documenta anche lo scopo e l'utilizzo. Il documento Parole chiave dello schema di stampa definisce anche istanze di diversi tipi di elementi, come indicato di seguito:

-   Istanze di proprietà e sottoproprietà che si trovano nella radice del documento PrintCapabilities

    -   Questi elementi descrivono i vari aspetti e funzionalità del dispositivo e forniscono un vocabolario comune per la descrizione dei dispositivi.

-   Istanze di proprietà e sottoproprietà che sono elementi figlio degli elementi Feature

    -   Questi elementi descrivono vari aspetti correlati a una funzionalità specifica.

-   Istanze di proprietà e sottoproprietà che sono elementi figlio degli elementi Option

    -   Questi elementi descrivono i vari aspetti e funzionalità del dispositivo che dipendono dall'opzione selezionata per una funzionalità specifica. Questi potrebbero essere sostituiti da istanze property che si trovano nella radice del documento PrintCapabilities, ma offrono maggiore praticità in alcuni casi. Per altre informazioni, vedere [Aggiunta di istanze di proprietà](adding-property-instances.md).

<!-- -->

-   Istanze scoredProperty

    -   Le istanze scoredProperty definiscono la lingua usata per caratterizzare un'opzione. Le istanze ScoredProperty definite nelle parole chiave dello schema di stampa rendono possibile che le istanze Option scritte da molte parti diverse per molti dispositivi siano portabili e siano comprese da qualsiasi altro driver di dispositivo o provider PrintCapabilities o PrintTicket.

-   Istanze di ScoredProperty Value

    -   Queste istanze Value vengono fornite per lo stesso motivo per cui vengono fornite le istanze scoredProperty.

-   Istanze di funzionalità

    -   Ogni opzione deve appartenere a una funzionalità specifica, richiedendo quindi la definizione della funzionalità stessa.

-   Istanze di ParameterDef

    -   Un'istanza ParameterDef fornita da parole chiave dello schema di stampa definisce anche un valore per ogni proprietà in essa contenuta. Il provider PrintCapabilities è libero di modificare le istanze Value per le istanze Property che possono essere modificate. Per informazioni sulle istanze Property che possono essere modificate e che non possono essere modificate (non modificabili), vedere [Elementi ParameterDef e ParameterInit](parameterdef-and-parameterinit-elements.md).

È importante notare che lo schema PrintCapabilities non denota alcuna istanza di Option. Le istanze di opzione sono caratterizzate esclusivamente dalle istanze ScoredProperty nel loro complesso. Un errore comune è che l'uso dell'attributo 'name' per definire un'opzione identifichi le istanze option, ma questo non è corretto. Gli elementi opzione non devono essere univoci per le istanze Option di pari livello né usano l'attributo 'name' per definire un'opzione obbligatoria.

Il documento Parole chiave dello schema di stampa definisce uno spazio dei nomi standard a cui appartengono tutti gli attributi del nome dell'istanza negli schemi PrintCapabilities e PrintTicket. Anche tutti i tag del tipo di elemento e gli attributi XML usati dai tipi di elemento appartengono a questo spazio dei nomi.

Per ogni istanza definita nello schema PrintCapabilities, lo schema PrintCapabilities specifica sia l'attributo name che il percorso dell'istanza. Il provider e il client devono mantenere entrambi quando si usa questa istanza nel documento PrintCapabilities o PrintTicket.

Il documento Print Schema Keywords (Parole chiave dello schema di stampa) definisce alcune istanze come obbligatorie. Queste istanze devono essere presenti in ogni documento PrintCapabilities e devono essere inizializzate correttamente con valori validi. Tutte le istanze nelle parole chiave dello schema di stampa non designate come obbligatorie sono facoltative.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



