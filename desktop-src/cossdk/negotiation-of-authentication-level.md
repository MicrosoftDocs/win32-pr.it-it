---
description: Negoziazione del livello di autenticazione
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: Negoziazione del livello di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b9983bd2a2df1d85cc6df4bfc0ba2a757b200f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305322"
---
# <a name="negotiation-of-authentication-level"></a>Negoziazione del livello di autenticazione

Sia il client che il server devono partecipare all'autenticazione e ogni entità indica che desidera eseguire un determinato livello di autenticazione. All'inizio di una chiamata, il livello di autenticazione viene negoziato tra le due parti, viene scelto un servizio appropriato e la chiamata viene autenticata e procede con la possibile crittografia, a seconda del livello di autenticazione scelto. Il livello di autenticazione negoziato tra il client e il server è determinato come massimo (*preferenza client*, *preferenza server*). L'effetto di questo significa che il server può sempre stabilire un livello minimo di autenticazione con cui è confortevole; ovvero l'autenticazione può essere dettata amministrativamente dal server.

Il client specifica che desidera eseguire l'autenticazione a un determinato livello come con qualsiasi applicazione COM. Il livello di autenticazione client può essere indicato come segue:

-   Per ogni computer client, con il livello di autenticazione COM a livello di computer impostato utilizzando [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) o lo strumento di amministrazione Servizi componenti.
-   Per applicazione client amministrativa, utilizzando [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) o lo strumento di amministrazione Servizi componenti se il client deve essere un'applicazione com+.
-   Per processo client a livello di codice, con [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   In qualsiasi momento a livello di codice, usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

L'applicazione server COM+ specifica un livello di autenticazione amministrativo utilizzando lo strumento di amministrazione Servizi componenti (o tramite uno script amministrativo).

La negoziazione dell'autenticazione per una chiamata procede nella sequenza seguente:

1.  Il livello di autenticazione viene scelto come MAX (*client*, *Server*).
2.  Negoziazione del protocollo di autenticazione.
3.  Il server autentica l'identità del client.
4.  Facoltativamente, il client autentica l'identità del server, a seconda del protocollo di autenticazione.
5.  Le chiamate al metodo vengono comunicate con il livello di autenticazione scelto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione client](client-authentication.md)
</dt> </dl>

 

 
