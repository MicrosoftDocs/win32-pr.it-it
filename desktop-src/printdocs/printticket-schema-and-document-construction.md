---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 573c2c82-aeb9-4ef2-8a1b-40b4db6ac6e4
title: Schema e costruzione di documenti PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe386638a7f119c52982f1911d602691455343f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234579"
---
# <a name="printticket-schema-and-document-construction"></a>Schema e costruzione di documenti PrintTicket

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il metodo corrente per specificare le informazioni di configurazione del dispositivo mediante una struttura DEVMODE soffre di diverse limitazioni. Innanzitutto, la struttura DEVMODE è una struttura binaria che può causare problemi di versioni diverse. In secondo luogo, è divisa in una parte pubblica non estendibile e una parte privata a cui è possibile accedere solo dai driver e solo dal driver specifico che lo ha creato. Il formato PrintTicket esprime le informazioni di configurazione utilizzando il Framework di Stampa schema basato su XML, eliminando così questi difetti della struttura DEVMODE.

Lo schema PrintTicket risolve ognuno dei due problemi appena citati. Innanzitutto, lo schema PrintTicket è un file di testo basato su XML, quindi vengono eliminati i problemi di estendibilità e controllo delle versioni. In secondo luogo, le informazioni di configurazione sono disponibili per tutti i client, vale a dire che qualsiasi client o provider può archiviare e recuperare tutte le informazioni contenute in un oggetto PrintTicket. Le opzioni vengono descritte utilizzando la stessa tecnica utilizzata dal Framework dello schema di stampa e dal documento PrintCapabilities derivato. Per questo motivo, l'oggetto PrintTicket fornisce tutti i potenziali vantaggi della portabilità del modello di definizione delle opzioni da realizzare. Per ulteriori informazioni, vedere [Print Schema Framework](print-schema-framework.md) . I destinatari di questa sezione includono i gruppi seguenti:

-   Implementatori di un'interfaccia del provider PrintTicket/PrintCapabilities

-   Utenti del PrintTicket

-   Client di un'interfaccia del provider PrintTicket/PrintCapabilities

I membri della prima categoria nell'elenco precedente sono definiti provider PrintTicket nella parte restante di questa sezione. I membri delle ultime due categorie sono definiti consumer PrintTicket.

## <a name="relationship-to-print-schema-and-printcapabilities-schema"></a>Relazione con schema di stampa e schema PrintCapabilities

Gli schemi PrintTicket e PrintCapabilities sono parti specializzate dello schema di stampa. La principale differenza strutturale tra questi subset dello schema di stampa è che lo schema PrintTicket contiene le istanze Property e ParameterInit che non sono contenute nello schema PrintCapabilities, mentre lo schema PrintCapabilities include le istanze Property e ParameterDef che non sono contenute nello schema PrintTicket. Ad eccezione di queste differenze, gli schemi PrintCapabilities e PrintTicket in genere si riflettono reciprocamente nelle istanze Content, sharing feature, Option, ScoredProperty e value. Ogni contenuto condiviso di questo tipo deve essere mantenuto aggiornato. Se, ad esempio, viene apportata una modifica alla funzionalità MediaSize nello schema PrintCapabilities, è necessario apportare la stessa modifica nello schema PrintTicket.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



