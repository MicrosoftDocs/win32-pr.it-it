---
description: Quando si creano scene 3D, un'applicazione può talvolta ottenere vantaggi in termini di prestazioni tramite il rendering di oggetti 2D in modo da sembrare oggetti 3D. Questa è l'idea di base alla base della tecnica del manifesto.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Manifesti pubblicitari (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02624a3172df7a36f4d38bb2bc6d613ded26faab8ac6d4f4b37668f0868cd16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123408"
---
# <a name="billboarding-direct3d-9"></a>Manifesti pubblicitari (Direct3D 9)

Quando si creano scene 3D, un'applicazione può talvolta ottenere vantaggi in termini di prestazioni tramite il rendering di oggetti 2D in modo da sembrare oggetti 3D. Questa è l'idea di base alla base della tecnica del manifesto.

Un manifesto nel senso normale della parola è un segno lungo una strada. Le applicazioni Microsoft Direct3D possono creare ed eseguire il rendering di questo tipo di manifesto definendo un solido rettangolare e applicando una trama. La grafica 3D è un'estensione di questo tipo. L'obiettivo è far sembrare 3D gli oggetti 2D. La tecnica consiste nell'applicare una trama che contiene l'immagine dell'oggetto a una primitiva rettangolare. La primitiva viene ruotata in modo da affrontare sempre l'utente. Non è importante se l'immagine dell'oggetto non è rettangolare. Le parti del manifesto possono essere rese trasparenti, quindi le parti dell'immagine del manifesto che non si vuole visualizzare non sono visibili.

Molti giochi impiegano la distribuzione di manifesti pubblicitari per gli sprite animati. Ad esempio, quando l'utente passa attraverso un labirinte 3D, può vedere le armi o le ricompense che possono essere ritirate. Si tratta in genere di immagini 2D con trama su una primitiva rettangolare. Il fumetto viene spesso usato nei giochi per eseguire il rendering di immagini di alberi, arbusti e cloud.

Quando un'immagine viene applicata a un manifesto pubblicitario, la primitiva rettangolare deve essere prima ruotata in modo che l'immagine risultante si faccia fronte all'utente. L'applicazione deve quindi tradurla in posizione. L'applicazione può quindi applicare una trama alla primitiva.

L'esecuzione di un manifesto è ideale per gli oggetti simmetrici, in particolare gli oggetti simmetrici lungo l'asse verticale. Richiede anche che l'altitudine del punto di vista non aumenti troppo. Se l'utente è autorizzato a visualizzare il manifesto dall'alto, diventa immediatamente evidente che l'oggetto è 2D anziché 3D.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di alfa](alpha-examples.md)
</dt> </dl>

 

 



