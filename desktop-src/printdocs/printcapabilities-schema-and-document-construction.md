---
title: Schemi e documenti PrintCapabilities
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1b8e2827e451fd8b1df477c33fe18d6203d10c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320882"
---
# <a name="printcapabilities-schema-and-document-construction"></a>Struttura del documento e dello schema PrintCapabilities

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le funzioni DevCaps Win32 correnti, ad esempio GetDeviceCaps o DeviceCapabilities, descritte nella documentazione di Microsoft Platform Software Development Kit (SDK), limitano gravemente il tipo di informazioni che i componenti non driver possono ottenere, in relazione alle funzionalità e alle proprietà dei dispositivi di stampa. Non è disponibile alcun supporto per la pubblicazione delle funzionalità dei processori di stampa, né un metodo per enumerare le funzionalità non standard. Pertanto non esiste alcun modo per un componente diverso da un driver per costruire un'interfaccia utente completa. Inoltre, il client o l'applicazione non è in grado di determinare completamente le funzionalità dei dispositivi o le code di stampa oltre a quelle fornite dalle funzioni Win32 DevCaps. Le funzioni correnti non sono estendibili, quindi i dispositivi non possono pubblicare nuove proprietà o funzionalità.

Lo schema PrintCapabilities ha lo scopo di eliminare molte delle limitazioni delle funzioni Win32 DevCaps fornendo un superset della funzionalità garantita da queste funzioni. Se sono necessarie più funzionalità, un provider del documento PrintCapabilities può estendere le parole chiave dello schema di stampa, all'interno dei vincoli di Print Schema Framework, aggiungendo istanze di elementi definite privatamente. A causa della dipendenza da XML come mezzo di interscambio, qualsiasi consumer di un documento PrintCapabilities può accedere a tutti i dati nel documento senza restrizioni e non è rilevante per la compatibilità con diverse versioni del sistema operativo. In questa sezione viene descritto lo schema PrintCapabilities e ne vengono illustrati i dettagli sull'utilizzo.

I destinatari di questa sezione includono i gruppi seguenti:

-   Implementatori dell'interfaccia del provider PrintTicket/PrintCapabilities

-   Utenti di PrintCapabilities

-   Client dell'interfaccia del provider PrintTicket/PrintCapabilities

La prima categoria nell'elenco precedente è indicata come provider PrintCapabilities nella parte restante di questa sezione. La seconda e la terza categoria sono denominate consumer PrintCapabilities.

## <a name="relationship-to-print-schema-and-printticket-schema"></a>Relazione con schema di stampa e schema PrintTicket

Gli schemi PrintCapabilities e PrintTicket sono parti specializzate dello schema di stampa. La principale differenza strutturale tra questi subset dello schema di stampa è che lo schema PrintCapabilities include le istanze Property e ParameterDef che non sono contenute nello schema PrintTicket, mentre lo schema PrintTicket contiene le istanze Property e ParameterInit che non sono contenute nello schema PrintCapabilities. Ad eccezione di queste differenze, gli schemi PrintCapabilities e PrintTicket in genere si riflettono reciprocamente nelle istanze Content, sharing feature, Option, ScoredProperty e value. Ogni contenuto condiviso di questo tipo deve essere mantenuto aggiornato. Se, ad esempio, viene apportata una modifica alla funzionalità PageMediaSize nello schema PrintCapabilities, è necessario apportare la stessa modifica nello schema PrintTicket.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



