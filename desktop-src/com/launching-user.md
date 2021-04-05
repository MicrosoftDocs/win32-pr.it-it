---
title: Avvio dell'utente
description: Avvio dell'utente
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872994"
---
# <a name="launching-user"></a>Avvio dell'utente

Si tratta dell'impostazione predefinita per l'identità dell'applicazione. Quando si sceglie l'utente di avvio per l'identità dell'applicazione, ogni account client ottiene una nuova istanza del server e ogni server ottiene la propria [finestra di Windows](/windows/desktop/winstation/window-stations). A causa delle istanze del server separate, l'avvio dell'utente è l'impostazione di identità di protezione di livello più alto. Tuttavia, esistono limiti limitati al consumo di risorse. Inoltre, tutte le GUI visualizzate dal server non saranno visualizzate dal client.

Se l'applicazione ha l'identità dell'utente che ha eseguito l'avvio, viene eseguita con un token di rappresentazione. Per ulteriori informazioni sui token di accesso e di rappresentazione, vedere [livelli di rappresentazione](impersonation-levels.md) e [mascheramento](cloaking.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Identità applicazione](application-identity.md)
</dt> <dt>

[Utente interattivo](interactive-user.md)
</dt> <dt>

[Identità del servizio](service-identity.md)
</dt> <dt>

[Utente specificato](specified-user.md)
</dt> </dl>

 

 