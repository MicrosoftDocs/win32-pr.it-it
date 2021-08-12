---
title: Account del servizio e BITS
description: È possibile usare BITS per trasferire file da un servizio. Il servizio deve usare l'account di sistema LocalSystem, LocalService o NetworkService. Questi account sono sempre connessi. Pertanto, i processi inviati da un servizio che usano questi account vengono sempre eseguiti.
ms.assetid: 43fb58d6-3a99-488f-ab43-dbb4a794fc2f
keywords:
- bits degli account del servizio
- trasferire il processo BITS, proprietà, account del servizio
- proxy BITS, account del servizio
- credenziali per trasferire BITS del processo
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: a996471afefb00b0dea87b07f477f5cab2fd29352c567dc9182fcf28fa5b168a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679903"
---
# <a name="service-accounts-and-bits"></a>Account del servizio e BITS

È possibile usare BITS per trasferire file da un servizio. Il servizio deve usare l'account di sistema LocalSystem, LocalService o NetworkService. Questi account sono sempre connessi. Pertanto, i processi inviati da un servizio che usano questi account vengono sempre eseguiti.

Se un servizio in esecuzione con un account di sistema rappresenta l'utente prima di chiamare BITS, BITS risponde come per qualsiasi account utente (ad esempio, l'utente deve essere connesso al computer per il trasferimento). Il servizio deve anche usare il cloaking dinamico con i puntatori all'interfaccia BITS durante la rappresentazione dell'utente. Il cloaking non viene ereditato, pertanto è necessario chiamare la funzione [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) su ogni puntatore a interfaccia ricevuto da BITS (ad esempio, il puntatore al processo restituito dalla chiamata al metodo [**IBackgroundCopyManager::CreateJob);**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) non è sufficiente impostare il cloaking sul puntatore a interfaccia di gestione. È anche possibile chiamare la [**funzione CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per il processo anziché chiamare la **funzione CoSetProxyBlanket** su ogni puntatore a interfaccia.

Tuttavia, se il servizio non rappresenta l'utente, si applicano i comportamenti seguenti:

- I processi creati dall'account del servizio appartengono a tale account. Poiché gli account di sistema sono sempre connessi, BITS trasferisce i file purché il computer sia in esecuzione e sia presente una connessione di rete.
- Gli account di sistema non devono usare lettere di unità di rete mappate perché le lettere di unità sono specifiche di una sessione e il mapping potrebbe andare perso dopo un riavvio del computer.
- In assenza di un [token helper,](helper-tokens-for-bits-transfer-jobs.md)l'autenticazione di rete usa le credenziali del computer per gli account LocalSystem e NetworkService e le credenziali anonime per l'account LocalService. BITS restituisce "accesso negato" se l'elenco di controllo di accesso (ACL) per il file di origine limita l'accesso a un account utente.
- Per informazioni dettagliate sul funzionamento dell'autenticazione in presenza di un [token helper,](helper-tokens-for-bits-transfer-jobs.md)vedere [Autenticazione](authentication.md).
- Microsoft Internet Explorer proxy vengono archiviate per utente e non sono impostate per gli account di sistema. Valutare la possibilità di configurare un token helper nei processi BITS o di impostare in modo esplicito le impostazioni proxy corrette chiamando [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **BG \_ JOB PROXY USAGE \_ \_ \_ OVERRIDE**. In alternativa, è possibile usare le opzioni **/Util /SetIEProxy** di BitsAdmin.exe per impostare Internet Explorer impostazioni proxy per l'account di sistema LocalSystem, LocalService o NetworkService. Per informazioni dettagliate, vedere [Strumento BitsAdmin](bitsadmin-tool.md).

Si noti che BITS non riconosce le impostazioni proxy impostate usando il Proxycfg.exe file.