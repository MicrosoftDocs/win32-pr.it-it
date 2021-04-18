---
title: Implementazione di Active Accessibility nativa
description: Gli elementi dell'interfaccia utente che implementano l'interfaccia IAccessible sono detti per fornire un'implementazione nativa.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5f6e6b6152c2f5e5c41a6a2b7cd3f84a3fce373
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298313"
---
# <a name="native-active-accessibility-implementation"></a>Implementazione di Active Accessibility nativa

Gli elementi dell'interfaccia utente che implementano l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sono detti per fornire un' *implementazione nativa*. Sebbene il costo di sviluppo per l'implementazione di **IAccessible** (o qualsiasi altra interfaccia Component Object Model (com)) possa essere elevato, il vantaggio è il controllo completo sulle informazioni esposte ai client.

Se l'applicazione usa controlli personalizzati o altri controlli che non possono essere inoltrati tramite proxy da Oleacc.dll, sarà necessario fornire un'implementazione nativa.

 

 




