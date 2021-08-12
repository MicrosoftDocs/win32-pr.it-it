---
description: Concetti relativi alle applicazioni di servizio COM+
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Concetti relativi alle applicazioni di servizio COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d0cedae4af19825e6e48a0e2aded102f96bed0c08b45c48cfb2f7e3bbd52ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548767"
---
# <a name="com-service-application-concepts"></a>Concetti relativi alle applicazioni di servizio COM+

È possibile usare lo strumento amministrativo Servizi componenti per configurare un'applicazione server COM+ come applicazione di servizio. L'esecuzione di un'applicazione server COM+ come servizio offre i vantaggi seguenti:

-   Se l'applicazione deve sempre essere in esecuzione, Servizi componenti può facoltativamente fare in modo che il server venga avviato automaticamente e può anche riavviare il server in caso di timeout. Ad esempio, se un computer che esegue componenti listener componenti in coda viene riavviato, i listener componenti in coda possono essere avviati automaticamente se sono configurati come servizio.
-   Se l'applicazione deve eseguire operazioni con privilegi, l'applicazione può essere eseguita come account di sistema locale. Solo i servizi NT possono essere eseguiti con questo livello di sicurezza. L'applicazione sarà compatibile con il Windows Servizio cluster, che gestisce i servizi durante il failover del sistema.
-   Se altri servizi devono essere contrassegnati come dipendenti, Servizi componenti fornisce questa opzione. Ad esempio, se l'applicazione usa funzionalità fornite da un altro servizio, il servizio contrassegnato come dipendente verrà avviato prima dell'avvio dell'applicazione.

## <a name="starting-an-application-automatically"></a>Avvio automatico di un'applicazione

Quando l'applicazione server COM+ viene avviata automaticamente, agisce come un servizio, richiedendo allo sviluppatore di gestire il server usando lo strumento amministrativo Servizi.

> [!Note]  
> Per accedere a Servizi, avviare lo strumento amministrativo Servizi componenti e quindi fare clic **su Servizi (locale)**.

 

## <a name="starting-an-application-manually"></a>Avvio manuale di un'applicazione

Quando l'applicazione server COM+ viene avviata manualmente, agisce come un host DLL con le impostazioni di sicurezza di un servizio. Il servizio verrà avviato manualmente quando viene attivato e arrestato automaticamente quando si verifica il timeout.

## <a name="service-configurations"></a>Configurazioni del servizio

Indipendentemente dal tipo di avvio, l'applicazione può essere configurata per l'esecuzione come account di sistema locale o assegnata a un account utente. Il sistema locale e l'account utente possono essere configurati al momento della creazione del servizio. Per configurare le impostazioni di sicurezza, sarà necessario usare lo strumento amministrativo Servizi. È anche possibile impostare le dipendenze per il servizio.

L'applicazione può anche essere avviata in un ordine specifico selezionando le dipendenze da un elenco di altri servizi di sistema. Ad esempio, i servizi di sistema possono essere contrassegnati come dipendenti e non avviano l'applicazione fino a quando i servizi di sistema non sono stati avviati nell'ordine specificato. In questo modo l'applicazione di servizio verrà inizializzata correttamente prima di essere usata.

Per istruzioni dettagliate su come configurare un'applicazione COM+ per l'esecuzione come servizio, vedere Configurazione di un'applicazione [server COM+](configuring-a-com--server-application-as-a-service-application.md)come applicazione di servizio .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività dell'applicazione di servizio COM+](com--service-application-tasks.md)
</dt> </dl>

 

 



