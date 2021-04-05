---
title: Errore comune che presuppone che RpcServerRegisterAuthInfo impedisca a utenti non autorizzati di chiamare il server
description: Quando i provider di sicurezza sono registrati nel server con la funzione RpcServerRegisterAuthInfo, viene aggiunta un'opzione, non un requisito.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713339"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a>Errore comune: supponendo che RpcServerRegisterAuthInfo impedisca a utenti non autorizzati di chiamare il server

Quando i provider di sicurezza sono registrati nel server con la funzione [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) , viene aggiunta un'opzione, non un requisito. Ciò significa che le registrazioni precedenti con **RpcServerRegisterAuthInfo** non vengono sostituite. Ciò significa anche che i client non autenticati possono ancora connettersi. Chiamando la funzione **RpcServerRegisterAuthInfo** , i client non autenticati non sono consentiti dalla connessione. possono comunque connettersi, ma le chiamate di funzione, ad esempio [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) , avranno esito negativo. Quindi, quando viene chiamata la funzione **RpcServerRegisterAuthInfo** , i potenziali utenti malintenzionati non sono stati eliminati, ma i client che dovrebbero avere accesso hanno la possibilità di dimostrare la propria identità. È necessario che siano ancora presenti controlli per determinare se i potenziali utenti malintenzionati tentano di connettersi.

 

 




