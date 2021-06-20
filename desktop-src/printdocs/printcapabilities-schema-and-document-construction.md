---
title: Schemi e documenti PrintCapabilities
description: Lo schema PrintCapabilities è progettato per eliminare molte delle limitazioni delle funzioni DevCaps Win32.
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21347fae1c9824df4a8355f8dd26de37eeac4604
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407074"
---
# <a name="printcapabilities-schema-and-document-construction"></a>Schema PrintCapabilities e costruzione di documenti

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le funzioni DevCaps Win32 correnti ( ad esempio GetDeviceCaps o DeviceCapabilities, entrambe descritte nella documentazione di Microsoft Platform Software Development Kit (SDK) ) limitano gravemente il tipo di informazioni che i componenti non driver possono ottenere, in relazione alle funzionalità e alle proprietà dei dispositivi di stampa. Non è disponibile alcun supporto per la pubblicazione delle funzionalità dei processori di stampa, né esiste un metodo per enumerare le funzionalità non standard. Non è quindi possibile che un componente diverso da un driver costruisca un'interfaccia utente completa. Inoltre, il client o l'applicazione non può determinare completamente le funzionalità dei dispositivi o delle code di stampa oltre a quelle fornite dalle funzioni Win32 DevCaps. Le funzioni correnti non sono estendibili, pertanto i dispositivi non possono pubblicare nuove proprietà o funzionalità.

Lo schema PrintCapabilities è progettato per eliminare molte delle limitazioni delle funzioni Win32 DevCaps fornendo un superset della funzionalità offerta da queste funzioni. Se sono necessarie altre funzionalità, un provider del documento PrintCapabilities può estendere le parole chiave dello schema di stampa, entro i vincoli di Print Schema Framework, aggiungendo istanze di elemento definite privatamente. A causa della sua attendibilità su XML come mezzo di interscambio, qualsiasi consumer di un documento PrintCapabilities può accedere a tutti i dati nel documento senza restrizioni e senza problemi di compatibilità con versioni diverse del sistema operativo. Questa sezione descrive lo schema PrintCapabilities e ne illustra in dettaglio l'uso.

Il gruppo di destinatari previsto per questa sezione include i gruppi seguenti:

-   Implementatori dell'interfaccia del provider PrintTicket/PrintCapabilities

-   Consumer di PrintCapabilities

-   Client dell'interfaccia del provider PrintTicket/PrintCapabilities

La prima categoria nell'elenco precedente viene definita provider PrintCapabilities nella parte restante di questa sezione. La seconda e la terza categoria sono definite consumer PrintCapabilities.

## <a name="relationship-to-print-schema-and-printticket-schema"></a>Relazione con schema di stampa e schema PrintTicket

Gli schemi PrintCapabilities e PrintTicket sono entrambe parti specializzate dello schema di stampa. Le principali differenze strutturali tra questi subset dello schema di stampa sono che lo schema PrintCapabilities include istanze Property e ParameterDef non contenute nello schema PrintTicket, mentre lo schema PrintTicket contiene istanze Property e ParameterInit che non sono contenute nello schema PrintCapabilities. Ad eccezione di queste differenze, gli schemi PrintCapabilities e PrintTicket in genere si rispecchiano tra loro nel contenuto, condividendo le istanze Feature, Option, ScoredProperty e Value. Qualsiasi contenuto condiviso di questo tipo deve essere mantenuto aggiornato. Ad esempio, se viene apportata una modifica alla funzionalità PageMediaSize nello schema PrintCapabilities, è necessario a questo punto a apportarne la stessa modifica nello schema PrintTicket.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



