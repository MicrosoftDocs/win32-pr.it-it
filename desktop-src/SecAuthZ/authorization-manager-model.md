---
description: Gestione autorizzazioni fornisce un'infrastruttura flessibile per l'integrazione del controllo di accesso basato sui ruoli nelle applicazioni. Consente agli amministratori che utilizzano tali applicazioni di fornire l'accesso tramite l'assegnazione di ruoli utente associati a qualifiche professionali.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Modello di Gestione autorizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20973b8b3e1b35780cc771c04302430b44352a112745842dcbdb66e92b948aad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784194"
---
# <a name="authorization-manager-model"></a>Modello di Gestione autorizzazioni

Gestione autorizzazioni fornisce un'infrastruttura flessibile per l'integrazione del controllo di accesso basato sui ruoli nelle applicazioni. Consente agli amministratori che utilizzano tali applicazioni di fornire l'accesso tramite l'assegnazione di ruoli utente associati a qualifiche professionali.

Le applicazioni di Gestione autorizzazioni consentono di archiviare criteri di autorizzazione in formato di archivi autorizzazioni che vengono archiviati in file XML o Active Directory e consentono di applicare criteri di autorizzazione in fase di esecuzione.

Le applicazioni chiamano quindi un metodo di controllo dell'accesso in fase di esecuzione che controlla l'accesso rispetto alle informazioni sui criteri nell'archivio autorizzazioni.

I criteri di autorizzazione includono le parti seguenti:

-   [Archivi criteri, applicazioni e ambiti](policy-stores--applications--and-scopes.md)
-   [Utenti e gruppi](users-and-groups.md)
-   [Operazioni e attività](operations-and-tasks.md)
-   [Ruoli](roles.md)
-   [Regole di business](business-rules.md)
-   [raccolte](collections.md)

 

 



