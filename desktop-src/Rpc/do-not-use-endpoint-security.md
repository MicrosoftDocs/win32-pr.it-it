---
title: Non usare la sicurezza degli endpoint
description: La sicurezza degli endpoint è un modello di sicurezza in cui viene fornito un descrittore di sicurezza quando viene creato un endpoint con il gruppo RpcServerUseProtseq\ di funzioni RPC.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d302ec0d331eaadb3291e36b30084264b4a6331745110fc642dd2ede02c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930698"
---
# <a name="do-not-use-endpoint-security"></a>Non usare la sicurezza degli endpoint

La sicurezza degli endpoint è un modello di sicurezza in cui viene fornito un descrittore di sicurezza quando viene creato un endpoint con il gruppo [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* di funzioni RPC. Non usare questo modello di sicurezza. Non assegnare descrittori di sicurezza a tali funzioni. Nel migliore dei modi, questo metodo è uno spreco di risorse della CPU. Nel peggiore dei casi, in molti ambienti è possibile aggirare il descrittore di sicurezza, come esemplifica la sezione Diffidare di altri [endpoint RPC in](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) esecuzione nello stesso processo.

La sicurezza degli endpoint esiste solo per la compatibilità con le versioni precedenti.

 

 




