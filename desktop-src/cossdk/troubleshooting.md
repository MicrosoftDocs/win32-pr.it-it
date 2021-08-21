---
description: Risoluzione dei problemi
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Risoluzione dei problemi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e10877306dc17f0b04718037a4bc073c8a7ed7c7c4ac46b31cda90517d22b7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812007"
---
# <a name="troubleshooting"></a>Risoluzione dei problemi

Se si verificano problemi durante la diagnosi degli errori dell'applicazione, vedere i suggerimenti per la risoluzione dei problemi seguenti:

-   Assicurarsi che il Distributed Transaction Coordinator (DTC) sia in esecuzione in tutti i server.
-   Controllare la comunicazione di rete testando prima in un computer locale per verificare che l'applicazione funzioni. Se si esegue TCP/IP nella rete, è possibile usare l'utilità ping.exe per verificare che i computer siano in rete.
-   Assicurarsi che SQL e DTC si trovino nello stesso computer o che il programma Configurazione client DTC specifichi che DTC si trova in un altro computer. In caso contrario, SQLConnect restituirà un errore internamente quando viene chiamato da un componente transazionale.
-   Impostare il timeout della transazione su un numero maggiore rispetto al valore predefinito di 60 secondi. Al termine del timeout della transazione, COM+ interrompe la transazione. Tutte le chiamate successive al componente restituiscono immediatamente context \_ E \_ ABORTED.
-   Assicurarsi che i driver ODBC siano thread-safe e non presentino affinità di thread.
-   Se si hanno difficoltà a far funzionare un'applicazione su più server, riavviare il client e quindi verificare che il controller di dominio sia configurato correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Isolamento degli errori e criteri failfast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Ricerca dell'origine di un errore](finding-the-source-of-an-error.md)
</dt> <dt>

[Modalità di modifica dei valori restituiti da COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretazione dei codici di errore](interpreting-error-codes.md)
</dt> <dt>

[Strategie per la gestione degli errori in COM+](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



