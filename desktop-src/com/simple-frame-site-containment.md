---
title: Contenimento semplice del sito di frame
description: Contenimento semplice del sito di frame
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955323"
---
# <a name="simple-frame-site-containment"></a>Contenimento semplice del sito di frame

Un controllo contenitore è un controllo ActiveX in grado di contenere altri controlli. Una casella di gruppo che contiene una raccolta di pulsanti di opzione è un esempio di un controllo contenitore. I controlli contenitore devono impostare il \_ bit di stato SIMPLEFRAME di OLEMISC e chiamare l'implementazione [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) del relativo contenitore. Un contenitore di controlli ActiveX che supporta i controlli contenitore deve implementare **ISimpleFrameSite**.

CATId-{157083E0-2368-11cf-87B9-00AA006C8166} CATId \_ SimpleFrameControl

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorie di componenti](component-categories.md)
</dt> </dl>

 

 




