---
description: Gestione autorizzazioni fornisce un'infrastruttura flessibile per l'integrazione del controllo di accesso basato sui ruoli nelle applicazioni. Consente agli amministratori che utilizzano tali applicazioni di fornire l'accesso tramite l'assegnazione di ruoli utente associati a qualifiche professionali.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Modello di gestione autorizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3455c9577f24b260bd02f947d0af99ec85570bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350611"
---
# <a name="authorization-manager-model"></a>Modello di gestione autorizzazioni

Gestione autorizzazioni fornisce un'infrastruttura flessibile per l'integrazione del controllo di accesso basato sui ruoli nelle applicazioni. Consente agli amministratori che utilizzano tali applicazioni di fornire l'accesso tramite l'assegnazione di ruoli utente associati a qualifiche professionali.

Le applicazioni di Gestione autorizzazioni consentono di archiviare criteri di autorizzazione in formato di archivi autorizzazioni che vengono archiviati in file XML o Active Directory e consentono di applicare criteri di autorizzazione in fase di esecuzione.

Le applicazioni chiamano quindi un metodo di verifica dell'accesso in fase di esecuzione che controlla l'accesso alle informazioni sui criteri nell'archivio autorizzazioni.

Il criterio di autorizzazione include le parti seguenti:

-   [Archivi, applicazioni e ambiti dei criteri](policy-stores--applications--and-scopes.md)
-   [Utenti e gruppi](users-and-groups.md)
-   [Operazioni e attività](operations-and-tasks.md)
-   [Ruoli](roles.md)
-   [Regole di business](business-rules.md)
-   [raccolte](collections.md)

 

 



