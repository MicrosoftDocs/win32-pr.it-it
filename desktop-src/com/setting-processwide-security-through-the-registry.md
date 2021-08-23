---
title: Impostazione Process-Wide sicurezza tramite il Registro di sistema
description: Se si vuole impostare la sicurezza per un intero processo, una soluzione consiste nell'impostare i livelli di sicurezza desiderati nel Registro di sistema.
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8ad3a549a78a10b15e965ba2e2a47b9e5e84f1e8790ccfbf90af622051714e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730911"
---
# <a name="setting-process-wide-security-through-the-registry"></a>Impostazione Process-Wide sicurezza tramite il Registro di sistema

Se si vuole impostare la sicurezza per un intero processo, una soluzione consiste nell'impostare i livelli di sicurezza desiderati nel Registro di sistema. Se l'applicazione non può [**chiamare CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o se si preferisce non usare la sicurezza a livello di codice, questa potrebbe essere un'opzione valida. Se si decide di impostare la sicurezza a livello di processo usando il Registro di sistema, è necessario tenere presente che se si chiama **CoInitializeSecurity** all'interno del programma COM userà i valori in **CoInitializeSecurity** e ignorerà i valori del Registro di sistema.

Esistono due modi per impostare la sicurezza nel Registro di sistema per l'applicazione:

-   È possibile usare Dcomcnfg.exe, che fornisce una semplice interfaccia utente per la modifica dei valori di sicurezza. Tutti i server COM possono essere configurati usando Dcomcnfg.exe. Per altre informazioni, vedere [Setting Process-Wide Security Using DCOMCNFG](setting-processwide-security-using-dcomcnfg.md). Tuttavia, le applicazioni client non vengono in genere visualizzate Dcomcnfg.exe a meno che il client non crei un GUID e lo immissione nel Registro di sistema.
-   È possibile impostare i valori di sicurezza nella [chiave AppID](appid-key.md) per l'applicazione. Il resto di questo argomento illustra come impostare la sicurezza nel Registro di sistema usando la **chiave AppID.**

Un AppID è un GUID che rappresenta un processo server per una o più classi. Ogni classe è associata esattamente a un AppID e gli AppID possono essere assegnati solo a ESE. Le DLL non ottengono Gli AppID a meno che non siano in esecuzione in un surrogato e quindi è il processo surrogato che ha l'AppID. Se più DLL vengono caricate in un surrogato, ogni surrogato ha un solo AppID.

Per alcuni server COM, il codice di registrazione genera un AppID e inserisce le voci nel Registro di sistema che e mappano l'AppID al nome dell'eseguibile. Tuttavia, alcuni server COM non forniscono questa funzionalità. Tuttavia, se il codice di registrazione del server aggiunge una voce per HKCR \\ CLSID{ServerCLSID} \\ [LocalServer32](localserver32.md) quando viene eseguito dcomcnfg.exe, aggiungerà automaticamente un AppID per il CLSID.

Per un client COM che non è un server, questo mapping non viene creato perché il client non viene mai registrato. Pertanto, per impostare la sicurezza usando la **chiave AppID,** il client deve [](/windows/desktop/SysInfo/registry-functions) creare le voci del Registro di sistema necessarie, a livello di codice usando le funzioni del Registro di sistema o regedit.

Se si decide di impostare la sicurezza a livello di processo nel Registro di sistema nella chiave **AppID,** tenere presente che nella chiave **AppID** sono presenti due valori denominati che è possibile impostare senza autorizzazioni di amministratore:

-   [AccessPermission](accesspermission.md)
-   [AuthenticationLevel](authenticationlevel.md)

I **valori AuthenticationLevel** **e AccessPermission** vengono impostati in modo indipendente e hanno valori predefiniti separati. Se il **valore AuthenticationLevel** non è presente, il [valore LegacyAuthenticationLevel](legacyauthenticationlevel.md) viene usato come valore predefinito. Analogamente, se il **valore AccessPermission** non è presente, il [valore DefaultAccessPermission](defaultaccesspermission.md) viene usato come valore predefinito. Tuttavia, i **valori AuthenticationLevel** e **AccessPermission** sono correlati nei modi seguenti:

-   Se **AuthenticationLevel non** è nessuno, i **valori AccessPermission** e **DefaultAccessPermission** vengono ignorati per l'applicazione.
-   Se **AuthenticationLevel non** è presente e **LegacyAuthenticationLevel** è none, i **valori AccessPermission** e **DefaultAccessPermission** vengono ignorati per l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione Process-Wide sicurezza](setting-processwide-security.md)
</dt> </dl>

 

 