---
title: Prevenzione della disconnessione o della sospensione durante un masterizzazione
description: Se non vengono prese precauzioni appropriate all'interno di un'applicazione, è possibile che un utente si disconti durante un'operazione di masterizzazione. Ciò comporta l'interruzione del processo di masterizzazione, che può comportare la perdita di dati e probabilmente rendere inutilizzabile il disco.
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f3dd6980db72854ff65d657cc58730335febcb1dbc8c4a467eedead88f5eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977131"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a>Prevenzione della disconnessione o della sospensione durante un masterizzazione

Se non vengono prese precauzioni appropriate all'interno di un'applicazione, è possibile che un utente si disconti durante un'operazione di masterizzazione. Ciò comporta l'interruzione del processo di masterizzazione, che può comportare la perdita di dati e probabilmente rendere inutilizzabile il disco.

Per evitare questo problema, l'applicazione deve elaborare il messaggio [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) che viene recapitato prima della disconnessione. Se l'applicazione riceve questo messaggio durante l'esecuzione di un'operazione di masterizzazione, restituire **FALSE per** annullare la procedura di disconnessione. Se l'applicazione consente all'utente di decidere se continuare la disconnessione, deve essere visualizzato un avviso che indica che l'utente perderà i dati.

Le transizioni di alimentazione durante il processo di masterizzazione possono anche creare potenziali problemi nel successo di un'attività di masterizzazione. Per evitare queste complicazioni durante il processo di masterizzazione, è necessario che un'applicazione sia a conoscenza del momento in cui stanno per verificarsi le transizioni di alimentazione. Questa operazione viene eseguita consentendo all'applicazione di elaborare il [**messaggio WM \_ POWERBROADCAST.**](/windows/desktop/Power/wm-powerbroadcast) Le applicazioni sviluppate per Windows XP o Windows Server 2003 possono restituire **BROADCAST \_ QUERY \_ DENY** in risposta a [**\_ PBT APMQUERYSUSPEND,**](/windows/desktop/Power/pbt-apmquerysuspend)impedendo la sospensione durante il processo di masterizzazione.

A causa delle modifiche apportate al modello di risparmio energia per Windows Vista e Windows Server 2008, l'evento [**\_ PBT APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) non viene più recapitato alle applicazioni. Viene invece [**recapitato \_ l'evento PBT APMSUSPEND,**](/windows/desktop/Power/pbt-apmsuspend) che fornisce due secondi per preparare un'applicazione per la transizione.

In seguito a queste modifiche, è consigliabile che le applicazioni chiamino la funzione [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) per evitare un timeout di inattività del sistema che in genere comporta la transizione a Suspend. È importante ricordare che la chiamata a questa funzione con i flag appropriati impostati impedirà solo l'inattività del sistema, non una sospensione in corso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di IMAPI](using-imapi.md)
</dt> <dt>

[**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 