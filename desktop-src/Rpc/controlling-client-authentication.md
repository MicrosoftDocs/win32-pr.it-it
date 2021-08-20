---
title: Controllo dell'autenticazione client
description: Il metodo migliore per autenticare un client è l'installazione di una funzione di callback di sicurezza usando la funzione RpcServerRegisterIf2 o RpcServerRegisterIfEx. accetta una funzione di callback di sicurezza come argomento.
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb00a03740d99b137f97b085525e4c7232483dc15db487daf486ad51560b4427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931238"
---
# <a name="controlling-client-authentication"></a>Controllo dell'autenticazione client

Il metodo migliore per autenticare un client è l'installazione di una funzione di callback di sicurezza usando la [**funzione RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) o [**RpcServerRegisterIfEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) accetta una funzione di callback di sicurezza come argomento. Quando viene chiamata la funzione di callback di sicurezza, effettuare i controlli necessari. È possibile controllare gli attributi della connessione, dell'identità del chiamante o di entrambi. Per controllare gli attributi di una connessione, chiamare la [**funzione RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) o [**RpcBindingInqAuthClient.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) In questo modo è possibile filtrare i client non autenticati, i client che usano un provider di sicurezza specifico o i client che non usano una protezione sufficientemente avanzata (ad esempio la privacy).

Per consentire l'accesso a un subset degli utenti autenticati, usare [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient). Questa funzione restituisce un contesto client Authz che può essere usato per eseguire controlli di accesso molto sofisticati. Ad esempio, questo metodo può essere usato per consentire l'accesso solo ai vicepresidenti di un'organizzazione durante le normali ore lavorative e al CEO durante qualsiasi ora usando i servizi Active Directory per eseguire il mapping di un nome utente al titolo. L'utente può essere rappresentato e il nome ottenuto. Una volta nota l'identità, è possibile eseguire i controlli desiderati.

 

 




