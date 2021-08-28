---
title: Avvio dell'utente
description: Avvio dell'utente
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e04163d5229942abff55339d53ba37ec0f8bdc6e9ac60b0893f1d243b22643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736537"
---
# <a name="launching-user"></a>Avvio dell'utente

Si tratta dell'impostazione predefinita per l'identità dell'applicazione. Quando l'utente che avvia viene scelto per l'identità dell'applicazione, ogni account client ottiene una nuova istanza del server e ogni server ottiene la propria [stazione finestra.](/windows/desktop/winstation/window-stations) A causa delle istanze del server separate, l'avvio dell'utente è l'impostazione dell'identità di protezione di livello superiore. Esistono tuttavia limiti finiti per l'utilizzo delle risorse. Inoltre, qualsiasi interfaccia utente grafica visualizzata dal server non verrà visualizzata dal client.

Se l'applicazione ha l'identità dell'utente che avvia, viene eseguita con un token di rappresentazione. Per altre informazioni sulla rappresentazione e sui token di accesso, vedere [Livelli di rappresentazione](impersonation-levels.md) e [Cloaking.](cloaking.md)

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

 

 