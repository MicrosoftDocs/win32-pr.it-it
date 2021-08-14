---
description: Il Windows di sicurezza consente ai chiamanti di Gestione transazioni kernel (KTM) di controllare l'accesso agli oggetti transazione, gestione transazioni, gestione risorse e integrazione.
ms.assetid: c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae
title: KTM Security and Access Rights
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0baf273b45a886e40c731c44c261f836fdc0b79012f906a1b4adfe07083be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388894"
---
# <a name="ktm-security-and-access-rights"></a>KTM Security and Access Rights

Il Windows di sicurezza consente ai chiamanti di Gestione transazioni kernel (KTM) di controllare l'accesso agli oggetti transazione, gestione transazioni, gestione risorse e integrazione. Per altre informazioni, vedere [Modello di controllo di accesso.](/windows/desktop/SecAuthZ/access-control-model) Per le applicazioni non interessate dalla sicurezza, è possibile creare transazioni con elenchi di controllo di accesso (ACL) permissivi che consentono a qualsiasi gestore di risorse di integrarsi in una transazione.

## <a name="transactions"></a>Transazioni

Quando un client usa la [**funzione OpenTransaction,**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza per l'oggetto transazione.

I diritti di accesso validi per gli oggetti transazione includono la possibilità di eseguire query e impostare le informazioni, l'integrazione e varie operazioni di transazione, nonché i [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights). [**Transaction Access Masks elenca**](transaction-access-masks.md) i diritti di accesso specifici per una transazione.

Poiché le transazioni hanno uno stato durevole, è fondamentale che le macchine virtuali e le macchine virtuali che interagiscono con la KTM soddis per quanto riguarda il ripristino. Il mancato adempimento di questi obblighi può comportare perdite di risorse che non vengono pulite, anche a causa di un riavvio del sistema. Considerare l'effetto di una perdita persistente o di codice dannoso che ha causato l'utilizzo delle risorse del kernel da parte della KTM fino a quando non si è verificato un errore di sistema. Dopo il riavvio risultante, KTM legge il log e rie crea nuovamente tutti gli oggetti persistenti, causando potenzialmente la ricorrenza dello stesso errore di sistema. La limitazione basata sulla quota impedirà l'affamazione persistente delle risorse da un RM non autorizzato o con comportamento non autorizzato. Infine, è necessario creare meccanismi amministrativi che consentano il rilevamento e la correzione di tali perdite persistenti.

## <a name="transaction-managers"></a>Gestori transazioni

Quando un client usa la [**funzione OpenTransactionManager,**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza per l'oggetto resource manager.

I diritti di accesso validi per gli oggetti di gestione transazioni includono la possibilità di eseguire query e impostare le informazioni, creare le macchine virtuali di ripristino, ripristinare e rinominare le operazioni, nonché i [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights). [**Transaction Manager Access Masks elenca**](transaction-manager-access-masks.md) i diritti di accesso specifici per un gestore transazioni.

Un gestore di risorse può creare i propri oggetti di gestione transazioni con ACL restrittivi per limitare i gestori di risorse che possono partecipare alle transazioni che utilizzano il log del gestore transazioni.

## <a name="resource-managers"></a>Resource Manager

Quando un client usa la [**funzione OpenResourceManager,**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza per l'oggetto resource manager.

I diritti di accesso validi per gli oggetti di Resource Manager includono la possibilità di eseguire query e impostare informazioni, recuperare, integrare, eseguire operazioni di registrazione e operazioni di propagazione e ripristino, nonché diritti di [accesso standard.](/windows/desktop/SecAuthZ/standard-access-rights) [**Resource Manager maschera di accesso elenca**](resource-manager-access-masks.md) i diritti di accesso specifici per un gestore di risorse.

Un gestore di risorse può creare i propri oggetti di gestione delle risorse con ACL restrittivi se vuole impedire a codice dannoso di intercettare le notifiche o forzare determinati risultati transazionali.

## <a name="enlistments"></a>Integrazioni

Quando un client usa la [**funzione OpenEnlistment,**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza per l'oggetto di integrazione.

I diritti di accesso validi per gli oggetti di integrazione includono la possibilità di eseguire query e impostare le informazioni, le operazioni di ripristino e i [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights). [**Enlistment Access Masks elenca**](enlistment-access-masks.md) i diritti di accesso specifici per un'integrazione.

 

 
