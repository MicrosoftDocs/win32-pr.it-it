---
description: Elementi replicati
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Elementi replicati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60b08151c14d0254bd856fe2ee5b7b83d85714d1b435a32817bf66cc11a1e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636651"
---
# <a name="what-gets-replicated"></a>Elementi replicati

## <a name="applications"></a>Applicazioni

Tutte le applicazioni installate nel computer di origine vengono replicate ad eccezione delle seguenti:

<dl> <dt>

<span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Elementi e dipendenze dell'applicazione non COM+
</dt> <dd>

L'amministratore è responsabile della replica di qualsiasi elemento da cui dipende un'applicazione COM+, ma che non fa correttamente parte dell'applicazione stessa, ad esempio file di dati e DLL. COMREPL non replica nulla all'esterno degli elementi dell'applicazione COM+.

</dd> <dt>

<span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Applicazioni COM+ preinstallate
</dt> <dd>

Le applicazioni usate internamente da COM+ e installate tramite il programma di installazione di COM+ non vengono replicate. tra cui:

-   Applicazione di sistema
-   Utilità COM+
-   Listener coda messaggi non recapiti com+ QC

</dd> <dt>

<span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applicazioni create da IIS
</dt> <dd>

Queste applicazioni non vengono replicate e includono quanto segue:

-   Applicazioni IIS in-process
-   Utilità IIS
-   Tutte le applicazioni create per radici virtuali isolate o in pool

</dd> </dl>

## <a name="computer-list"></a>Elenco computer

I computer remoti denominati nella **cartella Computer** dello strumento di amministrazione Servizi componenti non verranno replicati dal computer di origine a quello di destinazione.

## <a name="properties"></a>Proprietà

Vengono replicate le proprietà della raccolta **LocalComputer** seguenti:

-   TransactionTimeout
-   ResourcePoolingEnabled
-   DCOMEnabled
-   DefaultAuthenticationLevel
-   DefaultImpersonationLevel
-   SecurityTrackingEnabled
-   CISEnabled
-   SecureReferencesEnabled
-   InternetPortsListed
-   EsultToInternetPorts
-   Porte
-   RpcProxyEnabled

Le proprietà **della raccolta LocalComputer** seguenti non vengono replicate:

-   Descrizione
-   ApplicationProxyRSN
-   IsRouter

Per le descrizioni delle **proprietà della raccolta LocalComputer,** vedere [**LocalComputer.**](localcomputer.md)

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

 

 



