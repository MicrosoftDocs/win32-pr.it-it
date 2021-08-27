---
description: Questa sezione esamina una parte di un'applicazione di esempio che opera in rete molto lentamente. In questa sezione vengono apportate modifiche al codice iniziale per migliorarne le prestazioni.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Miglioramento di un'applicazione lenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff8f996267328805dc120d39218784a08383fb68ae9f6927e8983b6e1bec2d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097891"
---
# <a name="improving-a-slow-application"></a>Miglioramento di un'applicazione lenta

Questa sezione esamina una parte di un'applicazione di esempio che opera in rete molto lentamente. In questa sezione vengono apportate modifiche al codice iniziale per migliorarne le prestazioni.

L'esempio fittizio è la parte aggiornata per un gioco denominato Life. L'applicazione viene scritta in modo che il client esegua i calcoli per gli aggiornamenti e li invii al server. Il server visualizza quindi il campo Life risultante. L'output del client è un flusso di byte, raggruppati in tre (triplette), ognuna delle quali rappresenta un aggiornamento di una cella. I byte nella tripletta rappresentano rispettivamente la riga, la colonna e il valore della cella.

Questo esempio inizia come un'applicazione con prestazioni intenzionalmente scarse, che fornisce la baseline da cui è possibile illustrare i miglioramenti delle prestazioni. Da qui, il codice viene migliorato tre volte per risolvere vari problemi che influiscono sulle prestazioni. Questi esempi devono essere letti in ordine, in quanto ogni iterazione migliora la versione precedente.

Il codice di base e le revisioni che migliorano tale codice sono i seguenti:

-   [Versione di base: un'applicazione con prestazioni molto scarse](the-baseline-version-a-very-poor-performing-application-2.md)
-   [Revisione 1: Pulizia dell'ovvio](revision-1-cleaning-up-the-obvious-2.md)
-   [Revisione 2: Riprogettazione per un minor numero di connessione](revision-2-redesigning-for-fewer-connects-2.md)
-   [Revisione 3: Invio a blocchi compresso](revision-3-compressed-block-send-2.md)
-   [Miglioramenti futuri](future-improvements-2.md)

> [!WARNING]
> I primi esempi dell'applicazione offrono prestazioni intenzionalmente scarse, per illustrare i possibili miglioramenti delle prestazioni con le modifiche al codice. Non usare questi esempi di codice nell'applicazione. sono solo a scopo illustrativo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni socket Windows prestazioni elevate](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



