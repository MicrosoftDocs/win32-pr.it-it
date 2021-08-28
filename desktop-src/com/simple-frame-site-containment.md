---
title: Contenimento del sito con frame semplice
description: Contenimento del sito con frame semplice
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d356d6cc4993702ac571a800ad2abbfe378e8a8fe06ddc80225d81f0fe21a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129858"
---
# <a name="simple-frame-site-containment"></a>Contenimento del sito con frame semplice

Un controllo contenitore è ActiveX che è in grado di contenere altri controlli. Una casella di gruppo che contiene una raccolta di pulsanti di opzione è un esempio di controllo contenitore. I controlli contenitore devono impostare il bit di stato SIMPLEFRAME OLEMISC e \_ chiamare l'implementazione [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) del contenitore. Un ActiveX che supporta i controlli contenitore deve implementare **ISimpleFrameSite**.

CATID - {157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorie di componenti](component-categories.md)
</dt> </dl>

 

 




