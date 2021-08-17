---
description: Le applicazioni Direct3D usano la decalcommentazione per controllare quali pixel di una particolare immagine primitiva vengono disegnati sulla superficie di destinazione del rendering. Le applicazioni applicano decalcomanie alle immagini di primitive per consentire il rendering corretto dei poligoni coplanari.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Decaling (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e16b07eefcbf43bf2a3c71deb1a1073a656bb8d637696af71484a7a3e478ff8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117910217"
---
# <a name="decaling-direct3d-9"></a>Decaling (Direct3D 9)

Le applicazioni Direct3D usano la decalcommentazione per controllare quali pixel di una particolare immagine primitiva vengono disegnati sulla superficie di destinazione del rendering. Le applicazioni applicano decalcomanie alle immagini di primitive per consentire il rendering corretto dei poligoni coplanari.

Ad esempio, quando si applicano i segni di gomme e le linee gialle a una strada, i contrassegni devono essere visualizzati direttamente sopra la strada. Tuttavia, i valori z dei contrassegni e della strada sono gli stessi. Pertanto, il buffer di profondità potrebbe non produrre una netta separazione tra i due. È possibile eseguire il rendering di alcuni pixel nella primitiva posteriore sopra la primitiva anteriore e viceversa. L'immagine risultante viene visualizzata come s shi shi shi derivante da un frame all'altro. Questo effetto è denominato *z-fighting* o *fliluming.*

Per risolvere questo problema, usare uno stencil per mascherare la sezione della primitiva back in cui verrà visualizzata la decalcomania. Disattivare z-buffering ed eseguire il rendering dell'immagine della primitiva anteriore nell'area mascherata della superficie di destinazione di rendering.

Anche se è possibile usare la fusione di più trame per risolvere questo problema, questa operazione limita il numero di altri effetti speciali che l'applicazione può produrre. L'uso del buffer degli stencil per applicare le decalcomanie libera le fasi di fusione delle trame per altri effetti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche del buffer degli stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



