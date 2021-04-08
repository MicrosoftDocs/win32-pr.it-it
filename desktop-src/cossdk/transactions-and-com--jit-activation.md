---
description: Transazioni e attivazione JIT COM+
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transazioni e attivazione JIT COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878194"
---
# <a name="transactions-and-com-jit-activation"></a>Transazioni e attivazione JIT COM+

L'attivazione JIT COM+ è strettamente associata a transazioni automatiche. Quando si configura un componente in modo da richiedere una transazione o richiede una nuova transazione, viene abilitata automaticamente anche l'attivazione JIT. Le due funzionalità funzionano naturalmente insieme. I componenti con attivazione JIT transazionale condividono le caratteristiche seguenti:

-   Apolidia. Non si terrebbe lo stato che violerebbe l'isolamento delle transazioni, né lo stato che andrebbe perso per la disattivazione dell'oggetto.

-   Utilizzo rapido. Il modello di utilizzo canonico per un oggetto che esegue il lavoro in una transazione automatica consiste nell'eseguire alcune piccole unità di lavoro, voto ed uscita.

    > [!Note]  
    > Anche i modi in cui si votano le transazioni COM+ e l'operazione di segnalazione per l'attivazione JIT sono strettamente associati. Per ulteriori informazioni, vedere [impostazione del bit fatto](setting-the-done-bit.md).

     

-   Uso ripetuto. Quando il lavoro transazionale viene suddiviso correttamente, i client utilizzano gli stessi oggetti più volte per eseguire piccoli pacchi di lavoro atomico.

-   Disattivato in commit o Abort. In COM+ tutti gli oggetti all'interno del limite della transazione vengono disattivati quando viene eseguito il commit o l'interruzione della transazione.

Insieme ai componenti transazionali COM+, l'attivazione JIT funge da notevole miglioramento delle prestazioni mantenendo il canale aperto perché i client contengono riferimenti di lunga durata a oggetti transazionali. Per ulteriori miglioramenti, è possibile scegliere di raggruppare gli oggetti transazionali per riutilizzare le risorse in essi contenute, velocizzare il tempo di riattivazione degli oggetti e gestire in modo accurato la modalità di utilizzo delle risorse di memoria per gli oggetti specificati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione JIT di COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Abilitazione dell'attivazione JIT per un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Pool di oggetti e attivazione JIT COM+](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



