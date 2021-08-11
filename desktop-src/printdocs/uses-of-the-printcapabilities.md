---
description: Informazioni sugli usi di PrintCapabilities. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Usi di PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96aec2d21a2751305ae1f2e191a37adb584a0209542a78a0bf53253ea66faa20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233529"
---
# <a name="uses-of-the-printcapabilities"></a>Usi di PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

PrintCapabilities è progettato per rappresentare gli attributi del dispositivo configurabili come costrutti Feature/Option o costrutti di parametro. Queste informazioni definiscono lo spazio di configurazione del dispositivo e possono essere usate da un client dell'interfaccia utente per costruire un'interfaccia utente. Le parole chiave dello schema di stampa definiscono un set di istanze di funzionalità standard, istanze option per le istanze feature standard e istanze ParameterDef.

I costrutti di funzionalità/opzione o parametro in PrintCapabilities sono destinati a contenere istanze Property o ScoredProperty che descrivono un dispositivo e che sono supportate dal sottosistema spooler. Queste istanze Property e ScoredProperty sono di interesse generale per i client del dispositivo e contengono le informazioni fornite dalle funzioni Win32 DevCaps. Le parole chiave dello schema di stampa definiscono un set di istanze standard di Property e ScoredProperty.

È importante sottolineare che il documento PrintCapabilities è destinato a rappresentare solo dati a valore singolo: dati che non dipendono da una particolare configurazione del dispositivo. Il documento PrintCapabilities fornisce solo uno snapshot dei dati dipendenti dalla configurazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



