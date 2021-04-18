---
description: In questa sezione viene esaminata una parte di un'applicazione di esempio che opera sulla rete molto lentamente. In questa sezione vengono apportate modifiche al codice iniziale per migliorarne le prestazioni.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Miglioramento di un'applicazione lenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306951"
---
# <a name="improving-a-slow-application"></a>Miglioramento di un'applicazione lenta

In questa sezione viene esaminata una parte di un'applicazione di esempio che opera sulla rete molto lentamente. In questa sezione vengono apportate modifiche al codice iniziale per migliorarne le prestazioni.

L'esempio fittizio è la parte aggiornata per un gioco denominato Life. L'applicazione viene scritta in modo che il client esegua i calcoli per gli aggiornamenti e li invii al server. Il server Visualizza quindi il campo relativo alla durata risultante. L'output del client è un flusso di byte, raggruppati in tre (triplette), ognuno dei quali rappresenta un aggiornamento di una cella. I byte nella tripletta rappresentano rispettivamente la riga, la colonna e il valore per la cella.

Questo esempio inizia come un'applicazione intenzionalmente scadente, che fornisce la linea di base da cui è possibile illustrare i miglioramenti delle prestazioni. A questo punto, il codice è migliorato tre volte per risolvere vari problemi che influiscono sulle prestazioni. Questi esempi devono essere letti in ordine, in quanto ogni iterazione migliora la versione precedente.

Il codice di base e le revisioni che migliorano tale codice sono le seguenti:

-   [Versione di base: applicazione con prestazioni molto scarsa](the-baseline-version-a-very-poor-performing-application-2.md)
-   [Revisione 1: pulizia dell'ovvia](revision-1-cleaning-up-the-obvious-2.md)
-   [Revisione 2: riprogettazione per un minor numero di connessioni](revision-2-redesigning-for-fewer-connects-2.md)
-   [Revisione 3: invio blocco compresso](revision-3-compressed-block-send-2.md)
-   [Miglioramenti futuri](future-improvements-2.md)

> [!WARNING]
> I primi esempi dell'applicazione forniscono prestazioni intenzionalmente insoddisfacenti, per illustrare i miglioramenti delle prestazioni possibili con le modifiche al codice. Non usare questi esempi di codice nell'applicazione. sono solo a scopo illustrativo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni Windows Sockets a prestazioni elevate](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



