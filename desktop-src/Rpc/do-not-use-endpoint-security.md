---
title: Non utilizzare la sicurezza degli endpoint
description: Endpoint Security è un modello di sicurezza in cui viene fornito un descrittore di sicurezza quando viene creato un endpoint con il gruppo RpcServerUseProtseq \ di funzioni RPC.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289513810ba7e67e0da625151c3c2975e0eaaf99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709961"
---
# <a name="do-not-use-endpoint-security"></a>Non utilizzare la sicurezza degli endpoint

Endpoint Security è un modello di sicurezza in cui viene fornito un descrittore di sicurezza quando viene creato un endpoint con il gruppo [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* di funzioni RPC. Non utilizzare questo modello di sicurezza. Non assegnare descrittori di sicurezza a tali funzioni. Al meglio, questo metodo è uno spreco di risorse della CPU. Nel peggiore dei casi, in molti ambienti è possibile aggirare il descrittore di sicurezza, in quanto gli [altri endpoint RPC in esecuzione nella stessa](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) sezione del processo esemplificano.

La sicurezza degli endpoint esiste solo per la compatibilità con le versioni precedenti.

 

 




