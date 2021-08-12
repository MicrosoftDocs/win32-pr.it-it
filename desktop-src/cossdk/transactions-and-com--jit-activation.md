---
description: Transazioni e attivazione JIT COM+
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transazioni e attivazione JIT COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2b496f46652dc8ab9f6d573e712a0aa83575cac0adbb86a7dc4cfa88b565ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546048"
---
# <a name="transactions-and-com-jit-activation"></a>Transazioni e attivazione JIT COM+

L'attivazione JIT COM+ è strettamente associata alle transazioni automatiche. Quando si configura un componente in modo che richieda una transazione o richieda una nuova transazione, viene abilitata automaticamente anche l'attivazione JIT. Le due funzionalità funzionano naturalmente in combinazione. I componenti transazionali attivati tramite JIT condividono le caratteristiche seguenti:

-   Statelessness. Non è necessario mantenere lo stato che viola l'isolamento della transazione né lo stato che andrebbe perso in caso di disattivazione dell'oggetto.

-   Uso rapido. Il modello di utilizzo canonico per un oggetto che esegue operazioni in una transazione automatica è eseguire una piccola unità di lavoro, voto e uscita.

    > [!Note]  
    > Anche i modi in cui si vota nelle transazioni COM+ e la correttezza del segnale per l'attivazione JIT sono strettamente associati. Per altre informazioni, vedere [Impostazione del bit done](setting-the-done-bit.md).

     

-   Uso ripetuto. Quando il lavoro transazionale viene suddiviso correttamente, i client usano gli stessi oggetti più volte per eseguire piccole particelle di lavoro atomico.

-   Disattivato al commit o all'interruzione. In COM+, tutti gli oggetti all'interno del limite della transazione vengono disattivati quando la transazione esegue il commit o l'interruzione.

In combinazione con i componenti transazionali COM+, l'attivazione JIT funge da grande miglioramento delle prestazioni mantenendo aperto il canale man mano che i client contengono riferimenti di lunga durata agli oggetti transazionali. Come ulteriori miglioramenti, è possibile scegliere di eseguire il pool degli oggetti transazionali per riutilizzare le risorse che contengono, velocizzare il tempo di riattivazione degli oggetti e gestire da vicino il modo in cui si usano le risorse di memoria per oggetti specifici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione just-in-time di COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Abilitazione dell'attivazione JIT per un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Pool di oggetti e attivazione JIT COM+](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



