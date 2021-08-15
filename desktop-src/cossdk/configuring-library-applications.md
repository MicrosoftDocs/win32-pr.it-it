---
description: Configurazione di applicazioni di libreria
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Configurazione di applicazioni di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8ea0018d74070828384db25d76c73e7b5b3dba8a7dfc7d091c94e38aa0c3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047499"
---
# <a name="configuring-library-applications"></a>Configurazione di applicazioni di libreria

Poiché le applicazioni di libreria COM+ vengono eseguite nel processo del client, gli elementi configurabili per le applicazioni libreria sono notevolmente diversi rispetto alle applicazioni server. Non è possibile configurare alcun aspetto dell'applicazione determinato dal processo di hosting.

A livello di applicazione, diverse impostazioni sono limitate o non disponibili per le applicazioni di libreria. Questi vincoli sono descritti nella tabella seguente:



| Attributo                                       | Descrizione                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Livello di sicurezza<br/>                       | È necessario scegliere i controlli di accesso a livello di componente. L'applicazione libreria non può influire sui controlli di accesso a livello di processo. Vedere [Impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md).<br/>             |
| Abilitazione o disabilitazione dell'autenticazione<br/> | È possibile indicare se l'applicazione di libreria parteciperà all'autenticazione eseguita dal processo host. Vedere [Abilitazione dell'autenticazione per un'applicazione libreria](enabling-authentication-for-a-library-application.md).<br/> |
| Livello di rappresentazione<br/>                  | Disponibile. Viene usata l'impostazione del processo host. <br/>                                                                                                                                                                             |
| Identità di sicurezza<br/>                    | Disponibile. L'applicazione viene eseguita con l'identità del processo host.<br/>                                                                                                                                                          |
| Arresto del processo server<br/>              | Disponibile.<br/>                                                                                                                                                                                                                       |
| Abilitare il supporto di 3 GB<br/>                  | Disponibile.<br/>                                                                                                                                                                                                                       |
| Avviare nel debugger<br/>                   | Disponibile.<br/>                                                                                                                                                                                                                       |
| Abilitare CRM<br/>                           | Disponibile.<br/>                                                                                                                                                                                                                       |
| Accodamento<br/>                              | Disponibile.<br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'applicazione COM+](com--application-overview.md)
</dt> </dl>

 

 




