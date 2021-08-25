---
description: Eredità di transazioni manuali
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Eredità di transazioni manuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0042b7bb1e1545c44c44149c4605c9aabcbcc12fecebb974eb97f95da087b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896011"
---
# <a name="inheriting-manual-transactions"></a>Eredità di transazioni manuali

Se un oggetto con una transazione BYOT nel contesto crea un secondo oggetto, l'oggetto downstream può ereditare la transazione BYOT (se configurata per ereditare le transazioni). Il primo oggetto creato usando il gateway BYOT deve essere configurato per "richiedere" o "supportare" le transazioni. Gli oggetti successivi nell'attività possono essere configurati in base ai requisiti dell'applicazione.

Per le transazioni automatiche, il runtime COM+ non tenta di eseguire il commit della transazione fino a quando l'oggetto radice non indica che è pronto (chiamando [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) prima della restituzione da una chiamata). Gli utenti devono tenere presente che è possibile eseguire il commit prematuramente di una transazione BYOT (in quanto il lavoro degli oggetti figlio non è stato completato), perché la "radice" non è in esecuzione nell'ambiente di runtime COM+ e la semantica di commit non è associata alla durata dell'oggetto. In generale, l'utente deve fare attenzione a non violare il limite di sincronizzazione della transazione.

In caso contrario, viene applicata la semantica di commit COM+. COM+ non tenterà di eseguire il commit di una transazione mentre è in corso la chiamata di un oggetto all'interno di un limite di sincronizzazione. Inoltre, gli oggetti possono indicare la loro coerenza [**usando DisableCommit.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) Se si tenta di eseguire il commit di una transazione che include il lavoro di un oggetto denominato **DisableCommit**, la transazione verrà interrotta.

 

 



