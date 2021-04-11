---
description: Quando si utilizza la sicurezza basata sui ruoli, è possibile utilizzare l'oggetto contesto della chiamata di sicurezza per accedere alle informazioni di sicurezza sulla chiamata corrente.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Accesso alle informazioni sul contesto delle chiamate di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225716"
---
# <a name="accessing-security-call-context-information"></a>Accesso alle informazioni sul contesto delle chiamate di sicurezza

Quando si utilizza la sicurezza basata sui ruoli, è possibile utilizzare l'oggetto contesto della chiamata di sicurezza per accedere alle informazioni di sicurezza sulla chiamata corrente.

Dall'oggetto contesto della chiamata di sicurezza sono disponibili le seguenti raccolte di proprietà:

-   [Raccolta SecurityCallContext](#securitycallcontext-collection)
-   [Raccolta SecurityCallers](#securitycallers-collection)
-   [Raccolta SecurityIdentity](#securityidentity-collection)
-   [Argomenti correlati](#related-topics)

## <a name="securitycallcontext-collection"></a>Raccolta SecurityCallContext



| Proprietà                          | Descrizione                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| NumCallers<br/>             | Numero di chiamanti nella catena di chiamate.<br/>                                                                                |
| MinAuthenticationLevel<br/> | Livello di autenticazione meno sicuro di tutti i chiamanti nella catena.<br/>                                                          |
| Chiamanti<br/>                | Informazioni sull'identità dei chiamanti upstream, sotto forma di raccolta [**SecurityCallers**](securitycallers.md) .<br/> |
| DirectCaller<br/>           | Il chiamante che ha chiamato direttamente l'oggetto (senza chiamanti). <br/>                                                  |
| OriginalCaller<br/>         | Il chiamante che ha originato la catena di chiamate all'oggetto. <br/>                                                               |



 

Per ulteriori informazioni sull'utilizzo di questa raccolta, gli sviluppatori Microsoft Visual Basic dovrebbero vedere la classe [**SecurityCallContext**](securitycallcontext.md) . Gli sviluppatori C e C++ devono fare riferimento a [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).

## <a name="securitycallers-collection"></a>Raccolta SecurityCallers

La raccolta [**SecurityCallers**](securitycallers.md) rappresenta i chiamanti che possono essere recuperati tramite un indice compreso tra 0 e 1 minore di NumCallers, inclusi. Ogni chiamante è rappresentato da un oggetto [**SecurityIdentity**](securityidentity.md) .

Per ulteriori informazioni su questa raccolta, Visual Basic gli sviluppatori dovrebbero vedere la classe [**SecurityCallers**](securitycallers.md) . Gli sviluppatori C e C++ devono fare riferimento a [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).

## <a name="securityidentity-collection"></a>Raccolta SecurityIdentity



| Proprietà                         | Descrizione                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID<br/>                   | Identificatore di sicurezza per il chiamante.<br/>                                                                                                                   |
| AccountName<br/>           | Nome dell'account del chiamante.<br/>                                                                                                                           |
| AuthenticationService<br/> | Servizio di autenticazione utilizzato, ad esempio NTLMSSP, Kerberos o SSL.<br/>                                                                                       |
| AuthenticationLevel<br/>   | Livello di autenticazione utilizzato, che rappresenta la quantità di protezione utilizzata per la comunicazione con l'oggetto.<br/>                                         |
| ImpersonationLevel<br/>    | Livello di rappresentazione impostato dal client, se è stata utilizzata la rappresentazione. Questo livello indica la quantità di autorità assegnata al server dal client. <br/> |



 

Per ulteriori informazioni su questa raccolta, Visual Basic gli sviluppatori dovrebbero vedere la classe [**SecurityIdentity**](securityidentity.md) . Gli sviluppatori C e C++ devono fare riferimento a [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Verifica dell'appartenenza ai ruoli](checking-role-membership.md)
</dt> <dt>

[Determinare se Role-Based sicurezza è abilitata](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> </dl>

 

 




