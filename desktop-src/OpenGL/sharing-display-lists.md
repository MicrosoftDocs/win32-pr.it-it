---
title: Condivisione degli elenchi di visualizzazione
description: Quando si crea un contesto di rendering, dispone di un proprio spazio di visualizzazione elenco.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL per Windows, condivisione degli elenchi di visualizzazione
- condivisione degli elenchi di visualizzazione OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d8d012e8e04455f76ca5d7bfe74229ac0b0ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332060"
---
# <a name="sharing-display-lists"></a>Condivisione degli elenchi di visualizzazione

Quando si crea un contesto di rendering, dispone di un proprio spazio di visualizzazione elenco. La funzione [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) consente a un contesto di rendering di condividere lo spazio visualizzato nell'elenco di un altro contesto di rendering. Un qualsiasi numero di contesti di rendering può condividere un singolo spazio di visualizzazione elenco.

 

 




