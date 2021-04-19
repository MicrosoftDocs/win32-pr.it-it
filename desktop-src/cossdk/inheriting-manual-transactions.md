---
description: Eredità di transazioni manuali
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Eredità di transazioni manuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a802bb392223742e0116d34a81a25fe9be54f220
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304615"
---
# <a name="inheriting-manual-transactions"></a>Eredità di transazioni manuali

Se un oggetto con una transazione BYOT nel contesto crea un secondo oggetto, l'oggetto downstream può ereditare la transazione BYOT (se configurata per ereditare le transazioni). Il primo oggetto creato con il gateway BYOT deve essere configurato per le transazioni "require" o "Support". Gli oggetti successivi nell'attività possono essere configurati in base ai requisiti dell'applicazione.

Per le transazioni automatiche, il runtime COM+ non tenta di eseguire il commit della transazione fino a quando l'oggetto radice non indica che è pronto (chiamando il [**completamento**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) prima di tornare da una chiamata). Gli utenti devono tenere presente che una transazione BYOT potrebbe eseguire il commit in modo anomalo (in quanto il lavoro degli oggetti figlio non è stato completato), perché la "radice" non è in esecuzione nell'ambiente di runtime COM+ e la semantica di commit non è associata alla durata dell'oggetto. In generale, l'utente deve prestare attenzione a non violare il limite di sincronizzazione della transazione.

In caso contrario, viene applicata la semantica di commit COM+. COM+ non tenterà di eseguire il commit di una transazione mentre è in corso una chiamata a un oggetto all'interno di un limite di sincronizzazione. Gli oggetti possono inoltre indicare la loro coerenza usando [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit). Se viene effettuato un tentativo di eseguire il commit di una transazione che include il lavoro di un oggetto denominato **DisableCommit**, la transazione verrà interrotta.

 

 



