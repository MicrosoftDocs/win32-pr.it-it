---
description: Un AppContainer viene implementato mediante l'aggiunta di nuove informazioni al token del processo, modificando SeAccessCheck () in modo che tutti gli oggetti legacy, non modificati (ACL) di controllo di accesso blocchino le richieste di accesso dai processi AppContainer per impostazione predefinita e gli oggetti ACL che devono essere disponibili per AppContainers.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementazione di un AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884454"
---
# <a name="implementing-an-appcontainer"></a>Implementazione di un AppContainer

Un AppContainer viene implementato mediante l'aggiunta di nuove informazioni al token del processo, modificando [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) in modo che tutti gli oggetti legacy, non modificati (ACL) di controllo di accesso blocchino le richieste di accesso dai processi appcontainer per impostazione predefinita e gli oggetti ACL che devono essere disponibili per AppContainers.

## <a name="the-process"></a>Il processo

Per iniziare, aggiungere nuove informazioni per il token di processo. Modificare quindi **SeAccessCheck ()** in modo che tutti gli ACL legacy e non modificati blocchino le richieste di accesso dai processi appcontainer per impostazione predefinita. Infine, riacl risorse che devono essere disponibili per AppContainers

Il SID AppContainer è un identificatore univoco permanente per il appcontainer. I SID della funzionalità concedono l'accesso ai gruppi di risorse ai gruppi di AppContainers. Un AppContainerNumber è un **valore DWORD** temporaneo usato per distinguere tra AppContainers. Tuttavia, non deve essere usato come identità per AppContainer.

Per consentire a un singolo AppContainer di accedere a una risorsa, aggiungere il relativo AppContainerSID all'ACL per la risorsa.

Per consentire a più AppContainers specifiche di accedere a una risorsa, aggiungere tutti i AppContainerSIDs all'ACL per tale risorsa.

Per gestire i gruppi di autorizzazioni, creare un SID della funzionalità (un GUID) e inserire tale SID per tutte le risorse da concedere. Aggiungere quindi il SID funzionalità al token di processo.

Per consentire a tutti AppContainers di accedere a una risorsa, aggiungere il SID **tutti i pacchetti dell'applicazione** all'ACL per la risorsa. Questo comportamento è simile a un carattere jolly.

Sia AppContainerSID che CapabilitySID supportano le maschere di accesso nelle voci di controllo di accesso (ACE). Imposta come appropriato.

 

 
