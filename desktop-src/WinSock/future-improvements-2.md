---
description: Miglioramenti futuri per il codice dell'applicazione Winsock di esempio.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Miglioramenti futuri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306972"
---
# <a name="future-improvements"></a>Miglioramenti futuri

È possibile apportare diversi miglioramenti a questa applicazione, ad esempio:

-   Un'unica connessione persistente può essere creata dall'applicazione. È necessario aggiungere la gestione degli errori appropriata. In questo modo si riduce il sovraccarico associato all'avvio della connessione e a teardown.
-   Il codice di risposta sul server può essere ottimizzato per consolidare le risposte, riducendo il numero di pacchetti inviati dal server.
-   È possibile che siano stati apportati miglioramenti al protocollo. È possibile, ad esempio, utilizzare una maschera di aggiornamento per indicare le celle da aggiornare e solo i dati della cella inviati.
-   Gli aggiornamenti possono essere sovrapposti usando thread diversi, in modo che la rete non sia inattiva mentre è in esecuzione la funzione **ComputeNext** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento di un'applicazione lenta](improving-a-slow-application-2.md)
</dt> <dt>

[Versione di base: applicazione con prestazioni molto scarsa](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisione 1: pulizia dell'ovvia](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisione 2: riprogettazione per un minor numero di connessioni](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisione 3: invio blocco compresso](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



