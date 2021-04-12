---
description: L'API Authz consente alle applicazioni di eseguire controlli di accesso personalizzabili con prestazioni migliori e uno sviluppo più semplificato rispetto al controllo di accesso di basso livello.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Uso dell'API Authz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349706"
---
# <a name="using-authz-api"></a>Uso dell'API Authz

L'API Authz consente alle applicazioni di eseguire controlli di accesso personalizzabili con prestazioni migliori e uno sviluppo più semplificato rispetto [al controllo di accesso di basso livello](low-level-access-control.md).

L'API Authz consente alle applicazioni di memorizzare nella cache i controlli di accesso per migliorare le prestazioni, eseguire query e modificare i contesti dei client e definire regole business che possono essere usate per valutare in modo dinamico le autorizzazioni di accesso.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                             | Descrizione                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Inizializzazione di un contesto client](initializing-a-client-context.md)<br/>     | Un'applicazione deve creare un contesto client prima di poter usare l'API Authz per eseguire verifiche di accesso o controllo.<br/>                                                                                                                                            |
| [Esecuzione di query su un contesto client](querying-a-client-context.md)<br/>             | Le applicazioni possono chiamare la funzione [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) per eseguire query sulle informazioni relative a un contesto client esistente.<br/>                                                                                       |
| [Aggiunta di SID a un contesto client](adding-sids-to-a-client-context.md)<br/> | Un'applicazione può aggiungere [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) a un contesto client esistente chiamando la funzione [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .<br/> |
| [Verifica dell'accesso con l'API Authz](checking-access-with-authz-api.md)<br/>   | Le applicazioni determinano se concedere l'accesso agli oggetti a protezione diretta chiamando la funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .<br/>                                                                                                                |
| [Memorizzazione nella cache di controlli di accesso](caching-access-checks.md)<br/>                     | Quando un'applicazione esegue un controllo di accesso chiamando la funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , i risultati del controllo di accesso possono essere memorizzati nella cache.<br/>                                                                                       |



 

 

