---
title: Provider di sicurezza da usare
description: Tutti gli altri elementi sono uguali, usare RPC \_ C \_ AUTHN \_ GSS \_ KERBEROS o RPC C \_ \_ AUTHN \_ GSS \_ NEGOTIATE.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b89bdb10eb95952183b2a992fd12a668e79b0716f3c453f597d2241323c4ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010449"
---
# <a name="which-security-provider-to-use"></a>Provider di sicurezza da usare

Tutti gli altri elementi sono uguali, usare RPC \_ C \_ AUTHN \_ GSS \_ KERBEROS o RPC C \_ \_ AUTHN \_ GSS \_ NEGOTIATE. Ognuno offre il servizio più scalabile e sicuro. Se si usa RPC \_ C AUTHN GSS NEGOTIATE nel server, in questo modo i client di livello inferiore, ad esempio i client \_ \_ NTLM, possono \_ connettersi al server. Se ciò non è desiderato, limitare la scelta solo a \_ RPC C \_ AUTHN GSS KERBEROS oppure chiamare \_ \_ [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) per determinare il provider di sicurezza utilizzato dal client e negare l'accesso ai client tramite NTLM. Il metodo preferito per stabilire quale provider di sicurezza viene utilizzato dal client è la [**funzione RpcServerInqCallAttributes.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa)

 

 




