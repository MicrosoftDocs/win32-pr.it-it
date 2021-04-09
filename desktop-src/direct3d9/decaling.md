---
description: Le applicazioni Direct3D usano il decaing per controllare quali pixel di una determinata immagine primitiva vengono disegnati nell'area di destinazione del rendering. Le applicazioni applicano le decalcomanie alle immagini delle primitive per consentire il rendering corretto dei poligoni complanari.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Decaing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123876"
---
# <a name="decaling-direct3d-9"></a>Decaing (Direct3D 9)

Le applicazioni Direct3D usano il decaing per controllare quali pixel di una determinata immagine primitiva vengono disegnati nell'area di destinazione del rendering. Le applicazioni applicano le decalcomanie alle immagini delle primitive per consentire il rendering corretto dei poligoni complanari.

Ad esempio, quando si applicano segni di pneumatico e linee gialle a una carreggiata, i contrassegni devono essere visualizzati direttamente sopra la strada. Tuttavia, i valori z dei contrassegni e della strada sono gli stessi. Il buffer di profondità potrebbe pertanto non produrre una netta separazione tra i due. È possibile che venga eseguito il rendering di alcuni pixel della primitiva in primo piano sulla primitiva e viceversa. L'immagine risultante sembra riflessi da frame a frame. Questo effetto è detto *z-Fighting* o *flimmering*.

Per risolvere questo problema, usare uno stencil per mascherare la sezione della primitiva di sfondo in cui verrà visualizzata la decalcomania. Disattivare la memorizzazione nel buffer z ed eseguire il rendering dell'immagine della primitiva di primo piano nell'area nascosta della superficie di destinazione di rendering.

Sebbene sia possibile usare la combinazione di più trame per risolvere questo problema, limitare il numero di altri effetti speciali che l'applicazione può produrre. L'utilizzo del buffer di stencil per applicare le decalcomanie consente di liberare le fasi di combinazione delle trame per altri effetti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche del buffer dello stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



