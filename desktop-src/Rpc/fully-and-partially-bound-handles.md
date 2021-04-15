---
title: Handle con binding completo e parziale
description: Quando si usano gli endpoint dinamici, le librerie di runtime ottengono le informazioni sull'endpoint in modo necessario.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471323"
---
# <a name="fully-and-partially-bound-handles"></a>Handle con binding completo e parziale

Quando si usano gli endpoint dinamici, le librerie di runtime ottengono le informazioni sull'endpoint in modo necessario. Le librerie di runtime fanno distinzione tra un *handle completamente associato* (uno che include informazioni sull'endpoint) e un *handle parzialmente associato* (uno che non include informazioni sull'endpoint).

La libreria di runtime del client deve convertire l'handle parzialmente associato in un handle completamente associato prima che il client possa essere associato al server. La libreria di runtime del client tenta di convertire l'handle parzialmente associato per l'applicazione client ottenendo le informazioni sull'endpoint come illustrato:

-   Dalla specifica di interfaccia del client
-   Da un servizio di mapping degli endpoint in esecuzione nel server

Se il client tenta di utilizzare un handle parzialmente associato quando le informazioni sull'endpoint non sono disponibili nella specifica dell'interfaccia e l'endpoint mapper del server non dispone di informazioni sull'endpoint server, il client non dispone di informazioni sufficienti per eseguire la chiamata di procedura remota e la chiamata avrà esito negativo. Per evitare questo problema, è necessario registrare l'endpoint nel mapper di endpoint quando l'applicazione distribuita utilizza handle parzialmente associati. Per ulteriori informazioni sul mapper di endpoint, vedere [specifica di endpoint dinamici](specifying-endpoints.md).

Quando una chiamata di procedura remota ha esito negativo, l'applicazione client può chiamare [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) per rimuovere informazioni sull'endpoint non aggiornato. Quando il client tenta di chiamare la procedura remota, la libreria di runtime del client tenta nuovamente di convertire l'handle completamente associato in un handle parzialmente associato. Questa operazione è utile quando il server è stato arrestato e riavviato utilizzando un endpoint dinamico diverso.

 

 




