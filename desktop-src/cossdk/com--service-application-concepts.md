---
description: Concetti relativi all'applicazione del servizio COM+
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Concetti relativi all'applicazione del servizio COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483068"
---
# <a name="com-service-application-concepts"></a>Concetti relativi all'applicazione del servizio COM+

È possibile utilizzare lo strumento di amministrazione Servizi componenti per configurare un'applicazione server COM+ come applicazione di servizio. L'esecuzione di un'applicazione server COM+ come servizio offre i vantaggi seguenti:

-   Se è sempre necessario che l'applicazione sia in esecuzione, Servizi componenti può facoltativamente avviare automaticamente il server e riavviare il server in caso di timeout. Se, ad esempio, un computer che esegue componenti del listener dei componenti in coda viene riavviato, i listener di componenti in coda possono essere avviati automaticamente se sono configurati come servizio.
-   Se l'applicazione deve eseguire operazioni con privilegi, l'applicazione può essere eseguita come account di sistema locale. Con questo livello di sicurezza è consentita l'esecuzione solo dei servizi NT. L'applicazione sarà compatibile con la Servizio cluster di Windows che gestisce i servizi durante il failover del sistema.
-   Se gli altri servizi devono essere contrassegnati come dipendenti, Servizi componenti fornisce tale opzione. Se, ad esempio, l'applicazione usa la funzionalità fornita da un altro servizio, il servizio contrassegnato come dipendente verrà avviato prima dell'avvio dell'applicazione.

## <a name="starting-an-application-automatically"></a>Avvio automatico di un'applicazione

Quando l'applicazione server COM+ viene avviata automaticamente, funge da servizio, richiedendo allo sviluppatore la gestione del server tramite lo strumento di amministrazione servizi.

> [!Note]  
> Per accedere allo strumento di amministrazione servizi, è possibile avviare lo strumento di amministrazione Servizi componenti, quindi fare clic su **Servizi (locale)**.

 

## <a name="starting-an-application-manually"></a>Avvio manuale di un'applicazione

Quando l'applicazione server COM+ viene avviata manualmente, funge da host DLL con le impostazioni di sicurezza di un servizio. Il servizio verrà avviato manualmente quando viene attivato e arrestato automaticamente quando si verifica il timeout.

## <a name="service-configurations"></a>Configurazioni del servizio

Indipendentemente dal tipo di avvio, l'applicazione può essere configurata in modo da essere eseguita come account di sistema locale o assegnata a un account utente. Il sistema locale e l'account utente possono essere configurati al momento della creazione del servizio. Per configurare le impostazioni di sicurezza, sarà necessario utilizzare lo strumento di amministrazione servizi. Le dipendenze possono essere impostate anche per il servizio.

L'applicazione può anche essere avviata in un ordine particolare selezionando le dipendenze da un elenco di altri servizi di sistema. I servizi di sistema, ad esempio, possono essere contrassegnati come dipendenti e non avvieranno l'applicazione fino a quando i servizi di sistema non saranno stati avviati nell'ordine specificato. L'applicazione di servizio verrà inizializzata correttamente prima di essere utilizzata.

Per istruzioni dettagliate su come configurare un'applicazione COM+ per l'esecuzione come servizio, vedere [configurazione di un'applicazione server com+ come applicazione di servizio](configuring-a-com--server-application-as-a-service-application.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività delle applicazioni del servizio COM+](com--service-application-tasks.md)
</dt> </dl>

 

 



