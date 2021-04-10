---
title: Controllo dell'autenticazione client
description: Il metodo migliore per autenticare un client è l'installazione di una funzione di callback di sicurezza tramite la funzione RpcServerRegisterIf2 o RpcServerRegisterIfEx. accetta come argomento una funzione di callback di sicurezza.
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3508e99b351cd57fb67a3727710b60562ffe25dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856005"
---
# <a name="controlling-client-authentication"></a>Controllo dell'autenticazione client

Il metodo migliore per autenticare un client è l'installazione di una funzione di callback di sicurezza tramite la funzione [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) o [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) . accetta come argomento una funzione di callback di sicurezza. Quando viene chiamata la funzione di callback di sicurezza, effettuare i controlli necessari. È possibile controllare gli attributi sulla connessione, l'identità del chiamante o entrambi. Per controllare gli attributi di una connessione, chiamare la funzione [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) o [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) . In questo modo è possibile filtrare i client non autenticati, i client che utilizzano un provider di sicurezza specifico o i client che non utilizzano una protezione sufficientemente sicura (ad esempio la privacy).

Per consentire l'accesso a un subset di utenti autenticati, utilizzare [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient). Questa funzione restituisce un contesto client Authz che può essere usato per eseguire controlli di accesso molto sofisticati. Questo metodo, ad esempio, può essere utilizzato per consentire l'accesso solo ai vicepresidenti di un'organizzazione durante il normale orario di ufficio e al CEO durante un'ora utilizzando Active Directory Services per eseguire il mapping di un nome utente al titolo. L'utente può essere rappresentato e il nome ottenuto. Quando l'identità è nota, è possibile effettuare i controlli desiderati.

 

 




