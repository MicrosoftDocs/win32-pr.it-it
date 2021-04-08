---
description: Configurazione di applicazioni di libreria
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Configurazione di applicazioni di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51e00626d42044797881ccb86553ddfda38a089
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049139"
---
# <a name="configuring-library-applications"></a>Configurazione di applicazioni di libreria

Poiché le applicazioni di libreria COM+ vengono eseguite nel processo del client, gli elementi configurabili per le applicazioni di libreria sono notevolmente diversi rispetto alle applicazioni server. Non è possibile configurare alcun aspetto dell'applicazione determinato dal processo di hosting.

A livello di applicazione, diverse impostazioni sono limitate o non disponibili per le applicazioni di libreria. Questi vincoli sono descritti nella tabella seguente:



| Attributo                                       | Descrizione                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Livello di sicurezza<br/>                       | È necessario scegliere i controlli di accesso a livello di componente. L'applicazione di libreria non può influenzare i controlli di accesso a livello di processo. Vedere [impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md).<br/>             |
| Abilitazione o disabilitazione dell'autenticazione<br/> | È possibile indicare se l'applicazione della libreria parteciperà all'autenticazione eseguita dal processo host. Vedere [Abilitazione dell'autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md).<br/> |
| Livello di rappresentazione<br/>                  | Disponibile. Viene utilizzata l'impostazione del processo host. <br/>                                                                                                                                                                             |
| Identità di sicurezza<br/>                    | Disponibile. L'applicazione viene eseguita con l'identità del processo host.<br/>                                                                                                                                                          |
| Arresto del processo server<br/>              | Disponibile.<br/>                                                                                                                                                                                                                       |
| Abilita supporto da 3 GB<br/>                  | Disponibile.<br/>                                                                                                                                                                                                                       |
| Avvia nel debugger<br/>                   | Disponibile.<br/>                                                                                                                                                                                                                       |
| Abilita CRM<br/>                           | Disponibile.<br/>                                                                                                                                                                                                                       |
| Accodamento<br/>                              | Disponibile.<br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'applicazione COM+](com--application-overview.md)
</dt> </dl>

 

 




