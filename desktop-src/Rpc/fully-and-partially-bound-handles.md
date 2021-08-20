---
title: Handle completamente e parzialmente associati
description: Quando si usano endpoint dinamici, le librerie di runtime ottengono le informazioni sull'endpoint in base alle necessità.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f711955cedfba4359b910271f3ec5d77f4b383017eed8144e5201bb2d11cd3e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929649"
---
# <a name="fully-and-partially-bound-handles"></a>Handle completamente e parzialmente associati

Quando si usano endpoint dinamici, le librerie di runtime ottengono le informazioni sull'endpoint in base alle necessità. Le librerie di runtime fanno la distinzione tra un *handle* completamente associato (uno che include informazioni sull'endpoint) e un *handle* parzialmente associato (uno che non include le informazioni sull'endpoint).

La libreria di runtime del client deve convertire l'handle parzialmente associato in un handle completamente associato prima che il client possa eseguire l'associazione al server. La libreria di runtime client tenta di convertire l'handle parzialmente associato per l'applicazione client ottenendo le informazioni sull'endpoint come illustrato:

-   Dalla specifica dell'interfaccia del client
-   Da un servizio di mapping degli endpoint in esecuzione nel server

Se il client tenta di usare un handle parzialmente associato quando le informazioni sull'endpoint non sono disponibili nella specifica dell'interfaccia e il mapper di endpoint del server non dispone di informazioni sull'endpoint server, il client non avrà informazioni sufficienti per effettuare la chiamata di procedura remota e tale chiamata avrà esito negativo. Per evitare questo problema, è necessario registrare l'endpoint nel mapper di endpoint quando l'applicazione distribuita usa handle parzialmente associati. Per altre informazioni sul mapper di endpoint, vedere [Specifica di endpoint dinamici](specifying-endpoints.md).

Quando una chiamata di procedura remota ha esito negativo, l'applicazione client può chiamare [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) per rimuovere le informazioni sull'endpoint non aggiornate. Quando il client tenta di chiamare la procedura remota, la libreria di runtime del client prova di nuovo a convertire l'handle completamente associato in un handle parzialmente associato. Ciò è utile quando il server è stato arrestato e riavviato usando un endpoint dinamico diverso.

 

 




