---
description: Un AppContainer viene implementato aggiungendo nuove informazioni al token di processo, modificando SeAccessCheck() in modo che tutti gli oggetti elenco di controllo di accesso (ACL) legacy e non modificati blocchino le richieste di accesso dai processi AppContainer per impostazione predefinita e gli oggetti re-ACL che devono essere disponibili per AppContainer.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementazione di un AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d50c0a5aa9f80755084886554a533fe1c82a6791840a9ff4ea4fdcf1476fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670801"
---
# <a name="implementing-an-appcontainer"></a>Implementazione di un AppContainer

Un AppContainer viene implementato aggiungendo nuove informazioni al token di processo, modificando [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) in modo che tutti gli oggetti elenco di controllo di accesso (ACL) legacy e non modificati blocchino le richieste di accesso dai processi AppContainer per impostazione predefinita e gli oggetti re-ACL che devono essere disponibili per AppContainer.

## <a name="the-process"></a>Il processo

Iniziare aggiungendo nuove informazioni per il token del processo. Modificare quindi **SeAccessCheck() in** modo che tutti gli ACL legacy e non modificati blocchino le richieste di accesso dai processi AppContainer per impostazione predefinita. Infine, rielifinire l'elenco di controllo di accesso delle risorse che devono essere disponibili per AppContainers

Il SID di AppContainer è un identificatore univoco permanente per l'appcontainer. I SID di funzionalità concedono l'accesso a gruppi di risorse a gruppi di AppContainer. AppContainerNumber è un **valore DWORD temporaneo** usato per distinguere tra AppContainer. Tuttavia, non deve essere usato come identità per AppContainer.

Per consentire a un singolo AppContainer di accedere a una risorsa, aggiungere il relativo AppContainerSID all'elenco di controllo di accesso per tale risorsa.

Per consentire a diversi AppContainer specifici di accedere a una risorsa, aggiungere tutti i relativi AppContainerSID all'elenco di controllo di accesso per tale risorsa.

Per gestire i gruppi di autorizzazioni, creare un SID funzionalità (GUID) e inserire tale SID di funzionalità in tutte le risorse da concedere. Aggiungere quindi il SID funzionalità al token del processo.

Per consentire a tutti gli AppContainer di accedere a una risorsa, aggiungere il SID DI TUTTI **I** PACCHETTI DELL'APPLICAZIONE all'elenco di controllo di accesso per tale risorsa. Funziona come un carattere jolly.

Sia AppContainerSID che CapabilitySID supportano le maschere di accesso nelle voci di controllo di accesso (ACE). Impostare in base alle esigenze.

 

 
