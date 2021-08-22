---
title: Protezione del trasporto
description: Anche se questo non è il metodo preferito, è possibile usare le impostazioni di sicurezza offerte dal trasporto named pipe per aggiungere funzionalità di sicurezza all'applicazione distribuita.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d92a0c9f0b31392d265c1c60bd201d088af8e8ff0b10ac4e09e274da92d2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011209"
---
# <a name="transport-security"></a>Protezione del trasporto

Anche se questo non è il metodo preferito, è possibile usare le impostazioni di sicurezza offerte dal trasporto named pipe per aggiungere funzionalità di sicurezza all'applicazione distribuita. Queste impostazioni di sicurezza vengono usate con le funzioni RPC Microsoft che iniziano con i prefissi [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) e [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)e con le funzioni [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcRevertToSelf.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself)

> [!Note]  
> Se si esegue un'applicazione che è un servizio e si usa NTLM per la sicurezza, è necessario aggiungere una dipendenza esplicita del servizio per l'applicazione. Il Secur32.dll chiamerà Gestione controllo servizi (SCM) per avviare il servizio pacchetto di sicurezza NTLM. Tuttavia, un'applicazione RPC che è un servizio ed è in esecuzione come sistema, deve contattare anche SC a meno che non si connetta a un altro servizio nello stesso computer.

 

 

 




