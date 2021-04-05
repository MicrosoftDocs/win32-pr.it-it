---
title: Account del servizio e BITS
description: È possibile utilizzare BITS per trasferire file da un servizio. Il servizio deve usare l'account di sistema LocalSystem, LocalService o NetworkService. Questi account sono sempre connessi; di conseguenza, i processi inviati da un servizio usando questi account vengono sempre eseguiti.
ms.assetid: 43fb58d6-3a99-488f-ab43-dbb4a794fc2f
keywords:
- BITS degli account del servizio
- trasferimento di bit del processo, proprietà, account del servizio
- BIT proxy, account del servizio
- credenziali per il trasferimento di bit di processo
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 475a623e6b105d3ef2bdc6586db613c010fe8923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117918"
---
# <a name="service-accounts-and-bits"></a>Account del servizio e BITS

È possibile utilizzare BITS per trasferire file da un servizio. Il servizio deve usare l'account di sistema LocalSystem, LocalService o NetworkService. Questi account sono sempre connessi; di conseguenza, i processi inviati da un servizio usando questi account vengono sempre eseguiti.

Se un servizio in esecuzione con un account di sistema rappresenta l'utente prima di chiamare BITS, BITS risponde come per qualsiasi account utente (ad esempio, l'utente deve essere connesso al computer per consentire il trasferimento). Il servizio deve inoltre utilizzare il mascheramento dinamico con i puntatori dell'interfaccia BITS quando si rappresenta l'utente. Il cloaking non viene ereditato, pertanto è necessario chiamare la funzione [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) su ogni puntatore di interfaccia ricevuto da bit (ad esempio, il puntatore del processo restituito dalla chiamata al metodo [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) ); non è sufficiente impostare il cloaking sul puntatore dell'interfaccia del gestore. È anche possibile chiamare la funzione [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per il processo anziché chiamare la funzione **CoSetProxyBlanket** su ogni puntatore di interfaccia.

Tuttavia, se il servizio non rappresenta l'utente, si applicano i comportamenti seguenti:

- I processi creati dall'account del servizio appartengono a tale account. Poiché gli account di sistema sono sempre connessi, BITS trasferisce i file finché il computer è in esecuzione ed è presente una connessione di rete.
- Gli account di sistema non devono utilizzare lettere di unità di rete mappate perché le lettere di unità sono specifiche di una sessione e il mapping può andare perduto dopo il riavvio del computer.
- In assenza di un [token Helper](helper-tokens-for-bits-transfer-jobs.md), l'autenticazione di rete usa le credenziali del computer per gli account LocalSystem e NetworkService e le credenziali anonime per l'account LocalService. BITS restituisce "accesso negato" se l'elenco di controllo di accesso (ACL) per il file di origine limita l'accesso a un account utente.
- Per informazioni dettagliate sul funzionamento dell'autenticazione in presenza di un [token Helper](helper-tokens-for-bits-transfer-jobs.md), vedere [Authentication](authentication.md).
- Le impostazioni proxy di Microsoft Internet Explorer vengono archiviate per utente e non sono impostate per gli account di sistema. Valutare la possibilità di configurare un token helper nei processi BITS oppure di impostare in modo esplicito le impostazioni proxy corrette chiamando [**Metodo ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con la **sostituzione dell'utilizzo del \_ proxy del processo \_ \_ \_ BG**. In alternativa, è possibile utilizzare le opzioni **/util/SetIEProxy** di BitsAdmin.exe per impostare le impostazioni proxy di Internet Explorer per l'account di sistema LocalSystem, LocalService o NetworkService. Per informazioni dettagliate, vedere [lo strumento Bitsadmin](bitsadmin-tool.md).

Si noti che BITS non riconosce le impostazioni proxy impostate utilizzando il file di Proxycfg.exe.