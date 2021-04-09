---
title: Impostazione della sicurezza Process-Wide tramite il registro di sistema
description: Se si desidera impostare la sicurezza per un intero processo, una soluzione consiste nell'impostare i livelli di sicurezza desiderati nel registro di sistema.
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d303f184229cb20aef1cbf71733956a3b6ce6618
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963492"
---
# <a name="setting-process-wide-security-through-the-registry"></a>Impostazione della sicurezza Process-Wide tramite il registro di sistema

Se si desidera impostare la sicurezza per un intero processo, una soluzione consiste nell'impostare i livelli di sicurezza desiderati nel registro di sistema. Se l'applicazione non è in grado di chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o se si preferisce non usare la sicurezza a livello di codice, potrebbe trattarsi di un'opzione appropriata. Se si decide di impostare la sicurezza a livello di processo tramite il registro di sistema, è necessario tenere presente che se si chiama **CoInitializeSecurity** all'interno del programma com utilizzerà i valori in **CoInitializeSecurity** e ignorerà i valori del registro di sistema.

Esistono due modi per impostare la sicurezza nel registro di sistema per l'applicazione:

-   È possibile utilizzare Dcomcnfg.exe, che fornisce una semplice interfaccia utente per la modifica dei valori di sicurezza. Tutti i server COM possono essere configurati con Dcomcnfg.exe. Per ulteriori informazioni, vedere [impostazione di Process-Wide sicurezza tramite DCOMCNFG](setting-processwide-security-using-dcomcnfg.md). Tuttavia, le applicazioni client in genere non vengono visualizzate in Dcomcnfg.exe a meno che il client non crei un GUID e lo immetta nel registro di sistema.
-   È possibile impostare i valori di sicurezza sotto la chiave [AppID](appid-key.md) per l'applicazione. Nella parte restante di questo argomento viene illustrato come impostare la sicurezza nel registro di sistema utilizzando la chiave **AppID** .

Un AppID è un GUID che rappresenta un processo server per una o più classi. Ogni classe è associata esattamente a un AppID ed AppID può essere assegnato solo a exe. Le dll non ottengono AppID a meno che non siano in esecuzione in un surrogato, quindi è il processo surrogato con AppID. Se più DLL vengono caricate in un surrogato, ogni surrogato ha un solo AppID.

Per alcuni server COM, il codice di registrazione genera un AppID e inserisce le voci nel registro di sistema che mappano l'AppID al nome del file eseguibile. Tuttavia alcuni server COM non forniscono questa funzionalità. Tuttavia, se il codice di registrazione del server aggiunge una voce per HKCR \\ CLSID {ServerCLSID} \\ [LocalServer32](localserver32.md) quando viene eseguito dcomcnfg.exe, verrà aggiunto automaticamente un AppID per il CLSID.

Per un client COM che non è un server, questo mapping non viene creato perché il client non viene mai registrato. Per impostare la sicurezza tramite la chiave **AppID** , il client deve quindi creare le voci del registro di sistema necessarie, a livello di codice tramite le [funzioni del registro di sistema](/windows/desktop/SysInfo/registry-functions) o tramite regedit.

Se si decide di impostare la sicurezza a livello di processo nel registro di sistema nella chiave **AppID** , tenere presente che nella chiave **AppID** sono presenti due valori denominati che è possibile impostare senza disporre delle autorizzazioni di amministratore:

-   [AccessPermission](accesspermission.md)
-   [AuthenticationLevel](authenticationlevel.md)

I valori **AuthenticationLevel** e **AccessPermission** vengono impostati in modo indipendente e hanno valori predefiniti distinti. Se il valore di **AuthenticationLevel** non è presente, il valore di [LegacyAuthenticationLevel](legacyauthenticationlevel.md) viene usato come valore predefinito. Analogamente, se il valore **AccessPermission** non è presente, il valore di [DefaultAccessPermission](defaultaccesspermission.md) viene usato come valore predefinito. Tuttavia, i valori **AuthenticationLevel** e **AccessPermission** sono correlati nei modi seguenti:

-   Se **AuthenticationLevel** è None, i valori **AccessPermission** e **DefaultAccessPermission** vengono ignorati per l'applicazione.
-   Se **AuthenticationLevel** non è presente e **LegacyAuthenticationLevel** è None, i valori **AccessPermission** e **DefaultAccessPermission** vengono ignorati per l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 