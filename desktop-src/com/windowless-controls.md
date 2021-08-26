---
title: Controlli senza finestra
description: Controlli senza finestra
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf529349a1e1987870b3aac01a69aef3dacbd700d0060cd2177c05479409c7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991991"
---
# <a name="windowless-controls"></a>Controlli senza finestra

La ActiveX Controls 96 include una definizione per i controlli senza finestra. Questi controlli non funzionano nella propria finestra e richiedono un contenitore per offrire una finestra condivisa in cui il controllo può disegnare, vedere l'SDK ActiveX. I controlli senza finestra sono progettati per essere compatibili con i contenitori di controlli meno recenti creando una propria finestra in questa situazione, i contenitori di controlli senza finestra devono ospitare i controlli con finestra nel modo tradizionale senza problemi. Può tuttavia essere utile per un contenitore distinguere i controlli che possono operare in modalità senza finestra, quindi viene definita una categoria di componenti appropriata.

CATID - {1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID \_ WindowlessObject

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorie di componenti](component-categories.md)
</dt> </dl>

 

 




