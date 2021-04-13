---
title: Controlli senza finestra
description: Controlli senza finestra
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396919"
---
# <a name="windowless-controls"></a>Controlli senza finestra

La specifica ActiveX Controls 96 include una definizione per i controlli privi di finestra. Questi controlli non funzionano nella propria finestra e richiedono che un contenitore offra una finestra condivisa in cui il controllo può essere disegnato, vedere ActiveX SDK. I controlli privi di finestra sono progettati per essere compatibili con i contenitori di controllo meno recenti creando una propria finestra in questa situazione, i contenitori di controllo senza finestra devono ospitare controlli con finestra in modo tradizionale senza problemi. Può tuttavia essere utile per un contenitore distinguere i controlli che possono funzionare in modalità senza finestra, quindi viene definita una categoria di componenti appropriata.

CATId-{1D06B600-3AE3-11cf-87B9-00AA006C8166} CATId \_ WindowlessObject

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorie di componenti](component-categories.md)
</dt> </dl>

 

 




