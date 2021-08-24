---
title: Schemi e documenti PrintCapabilities
description: Lo schema PrintCapabilities è progettato per eliminare molte delle limitazioni delle funzioni Win32 DevCaps.
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd79c81beceecea4a660fd2376a759e470670a414a7cad4a8ac26be086688e15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711621"
---
# <a name="printcapabilities-schema-and-document-construction"></a>Schema PrintCapabilities e costruzione di documenti

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le funzioni DevCaps Win32 correnti( ad esempio GetDeviceCaps o DeviceCapabilities, entrambe descritte nella documentazione di Microsoft Platform Software Development Kit (SDK) ) limitano fortemente il tipo di informazioni che i componenti non driver possono ottenere, in relazione alle funzionalità e alle proprietà dei dispositivi di stampa. Non è disponibile alcun supporto per la pubblicazione delle funzionalità dei processori di stampa, né è disponibile un metodo per enumerare le funzionalità non standard. Non esiste quindi alcun modo per un componente diverso da un driver di costruire un'interfaccia utente completa. Inoltre, il client o l'applicazione non può determinare completamente le funzionalità dei dispositivi o delle code di stampa oltre a quelle fornite dalle funzioni Win32 DevCaps. Le funzioni correnti non sono estendibili, quindi i dispositivi non possono pubblicare nuove proprietà o funzionalità.

Lo schema PrintCapabilities è progettato per eliminare molte delle limitazioni delle funzioni DevCaps Win32 fornendo un superset della funzionalità offerta da queste funzioni. Se sono necessarie altre funzionalità, un provider del documento PrintCapabilities può estendere le parole chiave dello schema di stampa, entro i vincoli del framework dello schema di stampa, aggiungendo istanze di elemento definite privatamente. A causa della sua attendibilità su XML come mezzo di interscambio, qualsiasi consumer di un documento PrintCapabilities può accedere a tutti i dati nel documento senza restrizioni e senza problemi di compatibilità con versioni diverse del sistema operativo. Questa sezione descrive lo schema PrintCapabilities e ne illustra in dettaglio l'uso.

I destinatari di questa sezione includono i gruppi seguenti:

-   Implementatori dell'interfaccia del provider PrintTicket/PrintCapabilities

-   Consumer di PrintCapabilities

-   Client dell'interfaccia del provider PrintTicket/PrintCapabilities

La prima categoria nell'elenco precedente è denominata provider PrintCapabilities nella parte restante di questa sezione. La seconda e la terza categoria sono definite consumer PrintCapabilities.

## <a name="relationship-to-print-schema-and-printticket-schema"></a>Relazione con lo schema di stampa e lo schema PrintTicket

Gli schemi PrintCapabilities e PrintTicket sono entrambi parti specializzate dello schema di stampa. Le principali differenze strutturali tra questi subset dello schema di stampa sono che lo schema PrintCapabilities include istanze Property e ParameterDef non contenute nello schema PrintTicket, mentre lo schema PrintTicket contiene istanze Property e ParameterInit che non sono contenute nello schema PrintCapabilities. Ad eccezione di queste differenze, gli schemi PrintCapabilities e PrintTicket in genere si rispecchiano tra loro nel contenuto, condividendo le istanze Feature, Option, ScoredProperty e Value. Qualsiasi contenuto condiviso di questo tipo deve essere mantenuto aggiornato. Ad esempio, se viene apportata una modifica alla funzionalità PageMediaSize nello schema PrintCapabilities, la stessa modifica deve essere apportata nello schema PrintTicket.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



