---
description: Informazioni sul formato PrintTicket, che esprime le informazioni di configurazione usando il framework dello schema di stampa basato su XML.
ms.assetid: 573c2c82-aeb9-4ef2-8a1b-40b4db6ac6e4
title: Schema PrintTicket e costruzione di documenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5998aeb534bbbeb16681a4136cf33425a7eefad7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405434"
---
# <a name="printticket-schema-and-document-construction"></a>Schema PrintTicket e costruzione di documenti

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il metodo corrente per specificare le informazioni di configurazione del dispositivo usando una struttura DEVMODE presenta diverse limitazioni. In primo luogo, la struttura DEVMODE è una struttura binaria, che può causare problemi di versioni diverse. In secondo momento, è suddiviso in una parte pubblica non estensibile e in una parte privata accessibile solo dai driver e solo dal driver specifico che l'ha creata. Il formato PrintTicket esprime le informazioni di configurazione usando il framework dello schema di stampa basato su XML, eliminando così questi difetti della struttura DEVMODE.

Lo schema PrintTicket risolve ognuno dei due problemi appena menzionati. In primo luogo, lo schema PrintTicket è un file di testo basato su XML, quindi i problemi di estendibilità e controllo delle versioni vengono eliminati. In secondo momento, le informazioni di configurazione sono disponibili per tutti i client, vale a dire che qualsiasi client o provider può archiviare e recuperare qualsiasi informazione contenuta in un PrintTicket. Le opzioni vengono descritte usando la stessa tecnica usata dal framework dello schema di stampa e dal documento PrintCapabilities derivato. Per questo motivo, PrintTicket offre tutti i potenziali vantaggi di portabilità del modello di definizione dell'opzione da realizzare. Per [altre informazioni, vedere Print Schema Framework](print-schema-framework.md) . I destinatari di questa sezione includono i gruppi seguenti:

-   Implementatori di un'interfaccia del provider PrintTicket/PrintCapabilities

-   Consumer di PrintTicket

-   Client di un'interfaccia del provider PrintTicket/PrintCapabilities

I membri della prima categoria nell'elenco precedente sono definiti provider PrintTicket nella parte restante di questa sezione. I membri delle ultime due categorie sono definiti consumer PrintTicket.

## <a name="relationship-to-print-schema-and-printcapabilities-schema"></a>Relazione con lo schema di stampa e lo schema PrintCapabilities

Gli schemi PrintTicket e PrintCapabilities sono entrambi parti specializzate dello schema di stampa. Le principali differenze strutturali tra questi subset dello schema di stampa sono che lo schema PrintTicket contiene istanze Property e ParameterInit che non sono contenute nello schema PrintCapabilities, mentre lo schema PrintCapabilities include istanze Property e ParameterDef non contenute nello schema PrintTicket. Ad eccezione di queste differenze, gli schemi PrintCapabilities e PrintTicket in genere si rispecchiano tra loro nel contenuto, condividendo le istanze Feature, Option, ScoredProperty e Value. Qualsiasi contenuto condiviso di questo tipo deve essere mantenuto aggiornato. Ad esempio, se viene apportata una modifica alla funzionalità MediaSize nello schema PrintCapabilities, la stessa modifica deve essere apportata nello schema PrintTicket.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



