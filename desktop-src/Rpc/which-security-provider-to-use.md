---
title: Provider di sicurezza da usare
description: Tutti gli altri elementi sono uguali, usano RPC \_ c \_ AuthN \_ GSS \_ Kerberos o RPC \_ c \_ AuthN \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710570"
---
# <a name="which-security-provider-to-use"></a>Provider di sicurezza da usare

Tutti gli altri elementi sono uguali, usano RPC \_ c \_ AuthN \_ GSS \_ Kerberos o RPC \_ c \_ AuthN \_ GSS \_ Negotiate. Ogni fornisce il servizio più scalabile e sicuro. Se si usa \_ \_ \_ la negoziazione GSS C AuthN GSS \_ sul server, ciò consente ai client legacy, ad esempio i client NTLM, di connettersi al server. Se ciò non è auspicabile, limitare la scelta al solo tipo di autenticazione in base al protocollo di autenticazione basata su \_ \_ GSS di RPC C \_ \_ oppure chiamare [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) per determinare il provider di sicurezza utilizzato dal client e negare l'accesso ai client tramite NTLM. Il metodo preferito per stabilire il provider di sicurezza usato dal client è la funzione [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .

 

 




