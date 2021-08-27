---
description: I provider PrintCapabilities devono supportare un set minimo di funzionalità, implicite nell'interfaccia del provider PrintTicket/PrintCapabilities.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilità dei provider PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146082452c00c89c70768f641faaea97fee997fe01a20c0d99842bc5b961bfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470216"
---
# <a name="responsibilities-of-printcapabilities-providers"></a>Responsabilità dei provider PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

I provider PrintCapabilities devono supportare un set minimo di funzionalità, implicite nell'interfaccia del provider PrintTicket/PrintCapabilities. Queste funzionalità sono elencate qui.

-   Devono seguire la direzione della propagazione?? Attributo XML, quando viene visualizzato nel contesto appropriato e contiene un valore valido per tale contesto.

-   Devono generare un documento PrintCapabilities conforme allo schema PrintCapabilities e soddisfano i requisiti specificati nello schema di stampa.

-   Devono essere in grado di riconoscere un PrintTicket valido.

-   Devono essere in grado di interpretare un PrintTicket e comprendere la configurazione specifica che rappresenta.

-   Devono essere in grado di determinare se tale configurazione contiene conflitti di vincoli.

-   Devono essere in grado di modificare un PrintTicket non valido o in conflitto apportando la modifica meno significativa necessaria per renderla valida e senza conflitti.

-   Devono essere in grado di generare un documento PrintCapabilities per una particolare configurazione del dispositivo.

-   Devono essere in grado di generare una configurazione predefinita o PrintTicket.

-   Devono essere in grado di generare un documento PrintCapabilities corrispondente alla configurazione predefinita.

-   Devono implementare un processo di assegnazione dei punteggi delle opzioni definito dal driver di dispositivo in grado di determinare la vicinanza della corrispondenza tra due istanze option che appartengono alla stessa funzionalità. Questo algoritmo viene usato nel processo di convalida PrintTicket.

Oltre ai requisiti, il documento PrintCapabilities deve contenere valori validi e corretti per ogni attributo XML ,ad esempio vincolato, di ogni opzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



