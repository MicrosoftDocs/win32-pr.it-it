---
description: Cosa viene replicato
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Cosa viene replicato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304928"
---
# <a name="what-gets-replicated"></a>Cosa viene replicato

## <a name="applications"></a>Applicazioni

Tutte le applicazioni installate nel computer di origine vengono replicate ad eccezione di quanto segue:

<dl> <dt>

<span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Elementi e dipendenze dell'applicazione non COM +
</dt> <dd>

L'amministratore è responsabile della replica di qualsiasi elemento da cui dipende un'applicazione COM+, che non è parte integrante dell'applicazione stessa, ad esempio file di dati e dll. COMREPL non eseguirà la replica di alcun elemento all'esterno degli elementi dell'applicazione COM+.

</dd> <dt>

<span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Applicazioni preinstallate COM+
</dt> <dd>

Le applicazioni utilizzate internamente da COM+ e installate tramite il programma di installazione COM+ non vengono replicate. tra cui:

-   Applicazione di sistema
-   Utilità COM+
-   Listener coda messaggi non recapitabili di COM+ QC

</dd> <dt>

<span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applicazioni create da IIS
</dt> <dd>

Queste applicazioni non vengono replicate e includono quanto segue:

-   Applicazioni IIS in-process
-   Utilità IIS
-   Tutte le applicazioni create per le radici virtuali isolate o in pool

</dd> </dl>

## <a name="computer-list"></a>Elenco computer

I computer remoti denominati nella cartella **computer** dello strumento di amministrazione Servizi componenti non verranno replicati dal computer di origine al computer di destinazione.

## <a name="properties"></a>Proprietà

Vengono replicate le seguenti proprietà della raccolta **LocalComputer** :

-   TransactionTimeout
-   ResourcePoolingEnabled
-   DCOMEnabled
-   DefaultAuthenticationLevel
-   DefaultImpersonationLevel
-   SecurityTrackingEnabled
-   CISEnabled
-   SecureReferencesEnabled
-   InternetPortsListed
-   DeafultToInternetPorts
-   Porte
-   RpcProxyEnabled

Le seguenti proprietà della raccolta **LocalComputer** non vengono replicate:

-   Descrizione
-   ApplicationProxyRSN
-   Routing

Per le descrizioni delle proprietà della raccolta **LocalComputer** , vedere [**LocalComputer**](localcomputer.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei file](file-management.md)
</dt> <dt>

[Registrazione e segnalazione errori](logging-and-error-reporting.md)
</dt> <dt>

[Fasi di replica](replication-phases.md)
</dt> <dt>

[Uso di COMREPL](using-comrepl.md)
</dt> </dl>

 

 



