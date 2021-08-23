---
description: Quando si usa la sicurezza basata sui ruoli, l'oggetto contesto di chiamata di sicurezza può essere usato per accedere alle informazioni di sicurezza sulla chiamata corrente.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Accesso alle informazioni sul contesto delle chiamate di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e438ce3cfa137ece28bce70d2c820becede231b1b0381da38dd7c6bcc21cb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639121"
---
# <a name="accessing-security-call-context-information"></a>Accesso alle informazioni sul contesto delle chiamate di sicurezza

Quando si usa la sicurezza basata sui ruoli, l'oggetto contesto di chiamata di sicurezza può essere usato per accedere alle informazioni di sicurezza sulla chiamata corrente.

Le raccolte di proprietà seguenti sono disponibili dall'oggetto contesto di chiamata di sicurezza:

-   [Raccolta SecurityCallContext](#securitycallcontext-collection)
-   [Raccolta SecurityCallers](#securitycallers-collection)
-   [Raccolta SecurityIdentity](#securityidentity-collection)
-   [Argomenti correlati](#related-topics)

## <a name="securitycallcontext-collection"></a>Raccolta SecurityCallContext



| Proprietà                          | Descrizione                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| NumCallers<br/>             | Numero di chiamanti nella catena di chiamate.<br/>                                                                                |
| MinAuthenticationLevel<br/> | Livello di autenticazione meno sicuro di tutti i chiamanti nella catena.<br/>                                                          |
| Chiamanti<br/>                | Informazioni sull'identità dei chiamanti upstream, sotto forma di [**raccolta SecurityCallers.**](securitycallers.md)<br/> |
| DirectCaller<br/>           | Chiamante che ha chiamato direttamente l'oggetto (senza chiamanti interviene). <br/>                                                  |
| OriginalCaller<br/>         | Chiamante che ha originato la catena di chiamate all'oggetto . <br/>                                                               |



 

Per altre informazioni su come usare questa raccolta, microsoft Visual Basic gli sviluppatori dovrebbero vedere la [**classe SecurityCallContext.**](securitycallcontext.md) Gli sviluppatori C e C++ devono fare riferimento a [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).

## <a name="securitycallers-collection"></a>Raccolta SecurityCallers

La [**raccolta SecurityCallers**](securitycallers.md) rappresenta i chiamanti che possono essere recuperati usando un indice compreso tra 0 e 1 minore di NumCallers, inclusi. Ogni chiamante è rappresentato da [**un oggetto SecurityIdentity.**](securityidentity.md)

Per altre informazioni su questa raccolta, Visual Basic gli sviluppatori dovrebbero vedere la [**classe SecurityCallers.**](securitycallers.md) Gli sviluppatori C e C++ devono fare riferimento a [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).

## <a name="securityidentity-collection"></a>Raccolta SecurityIdentity



| Proprietà                         | Descrizione                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID<br/>                   | Identificatore di sicurezza per il chiamante.<br/>                                                                                                                   |
| AccountName<br/>           | Nome dell'account del chiamante.<br/>                                                                                                                           |
| Authenticationservice<br/> | Servizio di autenticazione usato, ad esempio NTLMSSP, Kerberos o SSL.<br/>                                                                                       |
| AuthenticationLevel<br/>   | Livello di autenticazione utilizzato, che rappresenta la quantità di protezione usata durante la comunicazione con l'oggetto .<br/>                                         |
| ImpersonationLevel<br/>    | Livello di rappresentazione impostato dal client, se è stata usata la rappresentazione. Questo livello indica la quantità di autorità data al server dal client. <br/> |



 

Per altre informazioni su questa raccolta, Visual Basic gli sviluppatori dovrebbero vedere la [**classe SecurityIdentity.**](securityidentity.md) Gli sviluppatori C e C++ devono fare riferimento a [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo dell'appartenenza al ruolo](checking-role-membership.md)
</dt> <dt>

[Determinare se Role-Based sicurezza è abilitata](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Sicurezza dei componenti a livello di codice](programmatic-component-security.md)
</dt> </dl>

 

 




