---
title: HKEY_LOCAL_MACHINESOFTWAREMicrosoftOle
description: I valori del Registro di sistema associati alla chiave HKEY LOCAL MACHINE SOFTWARE Microsoft Ole controllano le impostazioni predefinite delle autorizzazioni di avvio e accesso e le funzionalità di sicurezza a livello di chiamata per le applicazioni basate su COM che non \_ \_ chiamano \\ \\ \\ CoInitializeSecurity.
ms.assetid: 871ae88f-ed2c-4078-8160-b0a490390426
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1648f12cd3983c73f5fdae040d4b81a833cce64995d98c19ef804e2941af48e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993051"
---
# <a name="hkey_local_machinesoftwaremicrosoftole"></a>HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole

I valori del Registro di sistema associati alla **chiave HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ Ole** controllano le impostazioni predefinite delle autorizzazioni di avvio e accesso e le funzionalità di sicurezza a livello di chiamata per le applicazioni basate su COM che non chiamano [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

Solo gli amministratori, l'autore dell'oggetto e il sistema hanno accesso completo a questa parte del Registro di sistema. Tutti gli altri utenti hanno accesso in sola lettura.



| Valore del Registro di sistema                                                                         | Descrizione                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md)                 | Imposta il livello di dettaglio delle voci del log eventi relative alle richieste non riuscite per l'avvio e l'attivazione del componente.                                                                            |
| [**CallFailureLoggingLevel**](callfailurelogginglevel.md)                             | Imposta il livello di dettaglio delle voci del log eventi relative alle chiamate non riuscite ai componenti.                                                                                                     |
| [**DCOMSCMRemoteCallFlags**](dcomscmremotecallflags.md)                               | Controlla il comportamento delle chiamate da DCOM Service Control Manager (DCOMSCM) locale a un DCOMSCM remoto.                                                                     |
| [**DefaultAccessPermission**](defaultaccesspermission.md)                             | Definisce l'elenco di autorizzazioni di accesso predefinito per il computer.                                                                                                                      |
| [**DefaultLaunchPermission**](defaultlaunchpermission.md)                             | Definisce l'ACL di avvio predefinito per il computer.                                                                                                                                  |
| [**Enabledcom**](enabledcom.md)                                                       | Imposta i criteri di attivazione globali per il computer.                                                                                                                           |
| [**InvalidSecurityDescriptorLoggingLevel**](invalidsecuritydescriptorlogginglevel.md) | Imposta il livello di dettaglio delle voci del log eventi relative ai descrittori di sicurezza non validi per l'avvio del componente e le autorizzazioni di accesso.                                                       |
| [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)                         | Imposta il livello di autenticazione predefinito.                                                                                                                                        |
| [**LegacyImpersonationLevel**](legacyimpersonationlevel.md)                           | Imposta il livello di rappresentazione predefinito.                                                                                                                                         |
| [**LegacySecureReferences**](legacysecurereferences.md)                               | Determina il livello di sicurezza delle chiamate di versione **AddRef.** /                                                                                                               |
| [**MachineAccessRestriction**](machineaccessrestriction.md)                           | Imposta i criteri di restrizione a livello di computer per l'accesso ai componenti.                                                                                                               |
| [**MachineLaunchRestriction**](machinelaunchrestriction.md)                           | Imposta i criteri di restrizione a livello di computer per l'avvio e l'attivazione del componente.                                                                                                |
| [**NonRedist**](nonredist.md)                                                         | Aggiunge nomi all'elenco di file che non devono essere esportati quando le applicazioni COM+ vengono in pacchetto per l'installazione in altri computer. Si noti che si tratta di una sottochiave, non di un valore. |
| [**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)                   | Determina se i livelli di attendibilità dei criteri di restrizione software vengono usati durante le attivazioni ActivateAsActivator.                                                            |
| [**SRPRunningObjectChecks**](srprunningobjectchecks.md)                               | Determina se i tentativi di connessione agli oggetti in esecuzione vengono schermati per i livelli di attendibilità SRP (Software Restriction Policy) compatibili.                                         |



 

 

 




