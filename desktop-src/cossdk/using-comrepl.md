---
description: Uso di COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Uso di COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748639"
---
# <a name="using-comrepl"></a>Uso di COMREPL

Per avviare l'utilità da riga di comando COMREPL, attenersi alla procedura seguente:

1.  Aggiungere% windir% \\ system32 \\ com al percorso dell'ambiente predefinito digitando quanto segue nel prompt dei comandi:

    **set PATH =% PATH%;% WINDIR% \\ system32 \\ com**

2.  Immettere il comando COMREPL seguente:

    **Comrepl** *sourceComputer* *targetComputerList* **\[ \[ /n \] /v \]**

    dove:

    -   *sourceComputer* è il nome del computer di origine

    -   *targetComputerList* è il nome computer delle destinazioni separate da spazi

    -   **/n** disattiva la richiesta di conferma prima di avviare la replica

    -   **/v** restituisce l'output del file di log alla console

## <a name="notes"></a>Note

-   Poiché COM+ non viene replicato (solo dati di configurazione e applicazioni), in tutti i computer di destinazione deve essere già installato COM+.
-   L'utente deve passare i controlli dei ruoli per l'applicazione di sistema nei computer di origine e di destinazione.
-   Non sono stati replicati account computer locali che possono essere utilizzati dai ruoli.
-   I computer di destinazione devono essere online.
-   L'utente è responsabile della replica di tutti i dati non COM (ad esempio, tabelle di database, file di dati e così via) nei computer di destinazione.
-   I cluster possono partecipare alla replica, ma si noti che COMREPL viene replicato solo in computer denominati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei file](file-management.md)
</dt> <dt>

[Registrazione e segnalazione errori](logging-and-error-reporting.md)
</dt> <dt>

[Fasi di replica](replication-phases.md)
</dt> <dt>

[Cosa viene replicato](what-gets-replicated.md)
</dt> </dl>

 

 



