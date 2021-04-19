---
description: Risoluzione dei problemi
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Risoluzione dei problemi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304933"
---
# <a name="troubleshooting"></a>Risoluzione dei problemi

Se si verificano problemi durante la diagnosi degli errori dell'applicazione, vedere i suggerimenti per la risoluzione dei problemi seguenti:

-   Verificare che il Distributed Transaction Coordinator (DTC) sia in esecuzione in tutti i server.
-   Controllare la comunicazione di rete eseguendo il primo test in un computer locale per verificare che l'applicazione funzioni. Se si esegue TCP/IP nella rete, è possibile utilizzare l'utilità ping.exe per verificare che i computer siano in rete.
-   Verificare che SQL e DTC si trovino nello stesso computer o che il programma di configurazione del client DTC specifichi che DTC si trova in un altro computer. In caso contrario, SQLConnect restituirà un errore internamente quando viene chiamato da un componente transazionale.
-   Impostare il timeout della transazione su un numero superiore a quello predefinito di 60 secondi. Una volta trascorso il timeout della transazione, COM+ interrompe la transazione. Tutte le chiamate successive al componente vengono restituite immediatamente con contesto \_ E \_ interrotto.
-   Verificare che i driver ODBC siano thread-safe e che non abbiano affinità di thread.
-   Se si verificano problemi durante il funzionamento di un'applicazione su più server, riavviare il client e quindi verificare che il controller di dominio sia configurato correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Criteri di isolamento degli errori e FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Individuazione dell'origine di un errore](finding-the-source-of-an-error.md)
</dt> <dt>

[Modalità di modifica dei valori restituiti da COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretazione dei codici di errore](interpreting-error-codes.md)
</dt> <dt>

[Strategie per la gestione degli errori in COM+](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



