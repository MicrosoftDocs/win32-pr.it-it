---
title: Controlli contenitore
description: Controlli contenitore
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82048c02c6aa1db020a030f9a5a2fc92f0c5fc08914c930a315a97b31a88c120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896441"
---
# <a name="container-controls"></a>Controlli contenitore

Come descritto in precedenza, i controlli contenitore ActiveX che contengono visivamente altri controlli. L ActiveX dell'architettura dei controlli specifica [**l'interfaccia ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) per abilitare i controlli contenitore. I contenitori possono anche supportare i controlli contenitore senza il supporto **di ISimpleFrameSite,** anche se il comportamento non può essere garantito. Per questo motivo, esiste una categoria di componenti per i controlli SimpleFrameSite in cui è necessaria la funzionalità completa di questa interfaccia.

Per supportare i controlli contenitore senza implementare [**ISimpleFrameSite,**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)un ActiveX contenitore di controlli deve:

-   Attivare tutti i controlli in qualsiasi momento.
-   Riasparentare i controlli contenuti all'oggetto hWnd del controllo contenitore.
-   Mantenere l'elemento padre del controllo contenitore.

 

 




