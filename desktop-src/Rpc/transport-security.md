---
title: Protezione del trasporto
description: Sebbene questo non sia il metodo preferito, è possibile utilizzare le impostazioni di sicurezza offerte dal trasporto named pipe per aggiungere funzionalità di sicurezza all'applicazione distribuita.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d129b5a373ed7304c142c66dd0e8b2d4e9035416
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331476"
---
# <a name="transport-security"></a>Protezione del trasporto

Sebbene questo non sia il metodo preferito, è possibile utilizzare le impostazioni di sicurezza offerte dal trasporto named pipe per aggiungere funzionalità di sicurezza all'applicazione distribuita. Queste impostazioni di sicurezza vengono usate con le funzioni RPC di Microsoft che iniziano con i prefissi [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) e [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)e le funzioni [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

> [!Note]  
> Se si esegue un'applicazione che è un servizio e si usa NTLM per la sicurezza, è necessario aggiungere una dipendenza esplicita del servizio per l'applicazione. Il Secur32.dll chiamerà Gestione controllo servizi (SCM) per avviare il servizio del pacchetto di sicurezza NTLM. Tuttavia, un'applicazione RPC che è un servizio e viene eseguita come sistema, deve anche contattare il SC a meno che non si connetta a un altro servizio nello stesso computer.

 

 

 




