---
title: Prevenzione della disconnessione o della sospensione durante un'ustione
description: Se non vengono apportate precauzioni appropriate all'interno di un'applicazione, è possibile che un utente si disconnetta durante un'operazione di masterizzazione. Ciò comporta l'interruzione del processo di masterizzazione, che può causare la perdita di dati e possibilmente il rendering del disco inutilizzabile.
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5922fbe6dbc27303cee82e7ed745cbaaf2744781
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472875"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a>Prevenzione della disconnessione o della sospensione durante un'ustione

Se non vengono apportate precauzioni appropriate all'interno di un'applicazione, è possibile che un utente si disconnetta durante un'operazione di masterizzazione. Ciò comporta l'interruzione del processo di masterizzazione, che può causare la perdita di dati e possibilmente il rendering del disco inutilizzabile.

Per evitare questo problema, l'applicazione deve elaborare il messaggio [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) che viene recapitato prima della disconnessione. Se l'applicazione riceve questo messaggio durante l'esecuzione di un'operazione di masterizzazione, restituire **false** per annullare la procedura di disconnessione. Se l'applicazione consente all'utente di decidere se continuare la disconnessione, viene visualizzato un avviso che indica che l'utente perderà i dati.

Le transizioni di alimentazione durante il processo di masterizzazione possono anche creare potenziali problemi nel successo di un'attività Burn. Per evitare queste complicazioni durante il processo di masterizzazione, è necessario che un'applicazione sia a conoscenza del momento in cui si stanno verificando le transizioni di energia. Questa operazione viene eseguita tramite l'abilitazione dell'applicazione per l'elaborazione del messaggio [**WM \_ POWERBROADCAST**](/windows/desktop/Power/wm-powerbroadcast) . Le applicazioni sviluppate per Windows XP o Windows Server 2003 possono restituire la **query di trasmissione \_ \_ Deny** in risposta a [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend), impedendo la sospensione durante il processo di masterizzazione.

A causa delle modifiche apportate al modello di risparmio energia per Windows Vista e Windows Server 2008, l'evento [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) non viene più recapitato alle applicazioni. Viene invece recapitato l'evento [**PBT \_ APMSUSPEND**](/windows/desktop/Power/pbt-apmsuspend) , che fornisce due secondi per preparare un'applicazione per la transizione.

In seguito a queste modifiche, è consigliabile che le applicazioni chiamino la funzione [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) per impedire il timeout di inattività del sistema, che in genere comporta la sospensione della transizione. È importante ricordare che la chiamata a questa funzione con il set di flag appropriati impedisce solo l'inattività del sistema e non una sospensione in corso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di IMAPi](using-imapi.md)
</dt> <dt>

[**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 