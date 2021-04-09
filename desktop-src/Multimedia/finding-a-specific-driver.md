---
title: Ricerca di un driver specifico
description: Ricerca di un driver specifico
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- Gestione compressione audio (ACM), ricerca dei driver
- ACM (Gestione compressione audio), ricerca di driver
- Esempi di ACM, ricerca di driver
- ricerca di driver
- acmDriverEnum (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856754"
---
# <a name="finding-a-specific-driver"></a>Ricerca di un driver specifico

Potrebbe essere necessario che l'applicazione invii un messaggio direttamente a un driver specifico o per identificare determinati driver dall'elenco. È ad esempio possibile che l'applicazione identifichi i driver che supportano i filtri, quindi esegue una query su ogni driver per determinare quali tag di filtro sono supportati. È possibile utilizzare la funzione [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) per ottenere un handle per il driver o i driver desiderati. Questo handle può quindi essere utilizzato per comunicare con tale driver.

Si noti che quando un'applicazione installa un driver locale per uso personale, la funzione [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) restituisce un handle del driver, che può essere usato per comunicare con il driver. In questo caso, non è necessario usare **acmDriverEnum** .

 

 




