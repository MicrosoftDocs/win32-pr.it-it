---
description: Miglioramenti futuri al codice dell'applicazione Winsock di esempio.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Miglioramenti futuri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384d5a4f4ee9a4d6cb4a0f258d63262930dc5a6636be8d0e7f709b0e4f04e152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132364"
---
# <a name="future-improvements"></a>Miglioramenti futuri

Questa applicazione può essere migliorata in diversi modi, ad esempio:

-   L'applicazione può creare una singola connessione permanente. È necessario aggiungere la gestione degli errori appropriata. In questo modo si ridurrebbe il sovraccarico associato all'avvio e alla rimozione della connessione.
-   Il codice di risposta nel server può essere ottimizzato per consolidare le risposte, riducendo il numero di pacchetti inviati dal server.
-   È possibile apportare miglioramenti al protocollo. Ad esempio, è possibile usare una maschera di bit di aggiornamento per indicare quali celle devono essere aggiornate e solo i dati delle celle inviati.
-   Gli aggiornamenti possono essere sovrapposti usando thread diversi, in modo che la rete non sia inattiva durante l'esecuzione della funzione **ComputeNext.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento di un'applicazione lenta](improving-a-slow-application-2.md)
</dt> <dt>

[Versione di base: un'applicazione con prestazioni molto scarse](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisione 1: Pulizia dell'ovvio](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisione 2: Riprogettazione per un minor numero di connessione](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisione 3: Compressed Block Send](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



