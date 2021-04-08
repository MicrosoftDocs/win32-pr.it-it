---
title: HKEY_LOCAL_MACHINESOFTWAREMicrosoftOle
description: I valori del registro di sistema associati \_ al \_ software del computer locale HKEY \\ \\ Microsoft \\ OLE Key controllano le impostazioni di autorizzazione di avvio e accesso predefinite e le funzionalità di sicurezza a livello di chiamata per le applicazioni basate su com che non chiamano CoInitializeSecurity.
ms.assetid: 871ae88f-ed2c-4078-8160-b0a490390426
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02406bca5dd69098f8cd49c2fba5f067852fcc5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045276"
---
# <a name="hkey_local_machinesoftwaremicrosoftole"></a>\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE

I valori del registro di sistema associati al **\_ software del computer locale HKEY \_ \\ \\ Microsoft \\ OLE** Key controllano le impostazioni di autorizzazione di avvio e accesso predefinite e le funzionalità di sicurezza a livello di chiamata per le applicazioni basate su com che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Solo gli amministratori, l'autore dell'oggetto e il sistema hanno accesso completo a questa parte del registro di sistema. Tutti gli altri utenti hanno accesso in sola lettura.



| Valore del Registro di sistema                                                                         | Descrizione                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md)                 | Imposta il livello di dettaglio delle voci del registro eventi sulle richieste non riuscite per l'avvio e l'attivazione dei componenti.                                                                            |
| [**CallFailureLoggingLevel**](callfailurelogginglevel.md)                             | Imposta il livello di dettaglio delle voci del registro eventi sulle chiamate non riuscite ai componenti.                                                                                                     |
| [**DCOMSCMRemoteCallFlags**](dcomscmremotecallflags.md)                               | Controlla il comportamento delle chiamate da Gestione controllo servizi DCOM locale (DCOMSCM) a una DCOMSCM remota.                                                                     |
| [**DefaultAccessPermission**](defaultaccesspermission.md)                             | Definisce l'elenco delle autorizzazioni di accesso predefinito per il computer.                                                                                                                      |
| [**DefaultLaunchPermission**](defaultlaunchpermission.md)                             | Definisce l'ACL di avvio predefinito per il computer.                                                                                                                                  |
| [**EnableDCOM**](enabledcom.md)                                                       | Imposta i criteri di attivazione globali per il computer.                                                                                                                           |
| [**InvalidSecurityDescriptorLoggingLevel**](invalidsecuritydescriptorlogginglevel.md) | Imposta il livello di dettaglio delle voci del registro eventi relative a descrittori di sicurezza non validi per le autorizzazioni di avvio e accesso dei componenti.                                                       |
| [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)                         | Imposta il livello di autenticazione predefinito.                                                                                                                                        |
| [**LegacyImpersonationLevel**](legacyimpersonationlevel.md)                           | Imposta il livello di rappresentazione predefinito.                                                                                                                                         |
| [**LegacySecureReferences**](legacysecurereferences.md)                               | Determina il livello di sicurezza delle chiamate di / **rilascio** AddRef.                                                                                                              |
| [**MachineAccessRestriction**](machineaccessrestriction.md)                           | Imposta i criteri di restrizione a livello di computer per l'accesso al componente.                                                                                                               |
| [**MachineLaunchRestriction**](machinelaunchrestriction.md)                           | Imposta i criteri di restrizione a livello di computer per l'avvio e l'attivazione dei componenti.                                                                                                |
| [**NonRedist**](nonredist.md)                                                         | Aggiunge nomi all'elenco di file che non devono essere esportati quando le applicazioni COM+ sono assemblate per l'installazione in altri computer. Si noti che si tratta di una sottochiave, non di un valore. |
| [**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)                   | Determina se i livelli di attendibilità dei criteri di restrizione software vengono usati durante le attivazioni di ActivateAsActivator.                                                            |
| [**SRPRunningObjectChecks**](srprunningobjectchecks.md)                               | Determina se i tentativi di connessione agli oggetti in esecuzione vengono selezionati per i livelli di attendibilità dei criteri di restrizione software (SRP) compatibili.                                         |



 

 

 




