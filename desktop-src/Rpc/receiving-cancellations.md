---
title: Ricezione di annullamenti
description: L'applicazione server può chiamare RpcServerTestCancel con l'handle di associazione della chiamata in questione per determinare se il client ha richiesto l'annullamento della chiamata asincrona. Restituirà RPC \_ S OK se il client ha \_ annullato la chiamata.
ms.assetid: ac7d7a50-a788-40a9-b57d-1f528bdbd7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1757c2cac82b672504fc5aed5fe55a06d973a247c76d42e6f2a9debf1837d598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927119"
---
# <a name="receiving-cancellations"></a>Ricezione di annullamenti

L'applicazione server può chiamare [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) con l'handle di associazione della chiamata in questione per determinare se il client ha richiesto l'annullamento della chiamata asincrona. Restituirà RPC \_ S OK se il client ha \_ annullato la chiamata.

 

 




