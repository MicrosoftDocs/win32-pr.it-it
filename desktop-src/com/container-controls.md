---
title: Controlli contenitore
description: Controlli contenitore
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69228bcc03017442880d41156f67397ee26bb13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471787"
---
# <a name="container-controls"></a>Controlli contenitore

Come descritto in precedenza, i controlli contenitore sono controlli ActiveX che contengono visivamente altri controlli. L'architettura dei controlli ActiveX specifica l'interfaccia [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) per abilitare i controlli contenitore. I contenitori possono inoltre supportare i controlli contenitore senza supportare **ISimpleFrameSite**, anche se non è possibile garantire il comportamento. Per questo motivo, esiste una categoria di componenti per i controlli SimpleFrameSite in cui è necessaria la funzionalità completa di questa interfaccia.

Per supportare i controlli contenitore senza implementare [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), un contenitore di controlli ActiveX deve:

-   Attivare tutti i controlli in qualsiasi momento.
-   Eseguire un nuovo elemento padre dei controlli contenuti nell'hWnd del controllo che lo contiene.
-   Rimanere l'elemento padre del controllo contenitore.

 

 




