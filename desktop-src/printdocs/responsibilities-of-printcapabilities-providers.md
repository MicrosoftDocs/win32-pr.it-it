---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilità dei provider PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bbf355f7b62f8f9c8b3f3b0c59714cdd6ade5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320952"
---
# <a name="responsibilities-of-printcapabilities-providers"></a>Responsabilità dei provider PrintCapabilities

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

I provider PrintCapabilities devono supportare un set minimo di funzionalità, che sono implicite dall'interfaccia del provider PrintTicket/PrintCapabilities. Queste funzionalità sono elencate qui.

-   Devono seguire la direzione della propagazione? Attributo XML, quando viene visualizzato nel contesto appropriato e contiene un valore valido per tale contesto.

-   Devono generare un documento PrintCapabilities conforme allo schema PrintCapabilities e soddisfa i requisiti specificati nello schema di stampa.

-   Devono essere in grado di riconoscere un oggetto PrintTicket valido.

-   Devono essere in grado di interpretare un oggetto PrintTicket e comprendere la configurazione specifica che rappresenta.

-   Devono essere in grado di determinare se la configurazione contiene conflitti di vincolo.

-   Devono essere in grado di modificare un oggetto PrintTicket non valido o in conflitto eseguendo la modifica meno significativa necessaria per renderlo sia valido che senza conflitti.

-   Devono essere in grado di generare un documento PrintCapabilities per una particolare configurazione del dispositivo.

-   Devono essere in grado di generare una configurazione predefinita o un oggetto PrintTicket.

-   Devono essere in grado di generare un documento PrintCapabilities che corrisponde alla configurazione predefinita.

-   Devono implementare un processo di assegnazione dei punteggi delle opzioni definito dal driver di dispositivo in grado di determinare la chiusura della corrispondenza tra due istanze di opzioni che appartengono alla stessa funzionalità. Questo algoritmo viene utilizzato nel processo di convalida PrintTicket.

Oltre ai requisiti precedenti, il documento PrintCapabilities deve contenere valori validi e corretti per ogni attributo XML (ad esempio, vincolato) di ogni opzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



