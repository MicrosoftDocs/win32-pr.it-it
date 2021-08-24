---
description: Uso di COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Uso di COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501cca8d32383e23fc636669e32a80cfdfe96dd658717e41c1618244fc5af81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853881"
---
# <a name="using-comrepl"></a>Uso di COMREPL

Per avviare l'utilità della riga di comando COMREPL, seguire questa procedura:

1.  Aggiungere %windir% \\ system32 Com al percorso di \\ ambiente predefinito digitando quanto segue al prompt dei comandi:

    **set path = %PATH%;%windir% \\ system32 \\ Com**

2.  Immettere il comando COMREPL seguente:

    **ORIGINE COMREPLComputer**  *targetComputerList* **\[ /n \[ /v \] \]**

    dove:

    -   *sourceComputer* è il nome computer dell'origine

    -   *targetComputerList* è il nome computer delle destinazioni separate da spazi

    -   **/n elimina** la richiesta di conferma prima di avviare la replica

    -   **/v** genera l'output del file di log nella console

## <a name="notes"></a>Note

-   Poiché COM+ non viene replicato (solo i dati di configurazione e le applicazioni), in tutti i computer di destinazione deve essere già installato COM+.
-   L'utente deve passare i controlli dei ruoli per l'applicazione di sistema nei computer di origine e di destinazione.
-   Non viene replicato alcun account computer locale che possa essere usato dai ruoli.
-   I computer di destinazione devono essere online.
-   L'utente è responsabile della replica di tutti i dati non COM+, ad esempio tabelle di database, file di dati e così via, nei computer di destinazione.
-   I cluster possono partecipare alla replica, ma si noti che COMREPL viene replicato solo in computer denominati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei file](file-management.md)
</dt> <dt>

[Registrazione e segnalazione errori](logging-and-error-reporting.md)
</dt> <dt>

[Fasi di replica](replication-phases.md)
</dt> <dt>

[Elementi replicati](what-gets-replicated.md)
</dt> </dl>

 

 



