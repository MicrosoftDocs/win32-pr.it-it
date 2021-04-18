---
description: 'In genere, le applicazioni grafiche 3D utilizzano due tipi di sistemi di coordinate cartesiane: a sinistra e a destra.'
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: Sistemi di coordinate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb9fa389b2bf11bec9ee4f8053bbeb4c822f422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304549"
---
# <a name="coordinate-systems-direct3d-9"></a>Sistemi di coordinate (Direct3D 9)

In genere, le applicazioni grafiche 3D utilizzano due tipi di sistemi di coordinate cartesiane: a sinistra e a destra. In entrambi i sistemi di coordinate, l'asse x positivo punta a destra e l'asse y positivo punta verso l'alto. È possibile ricordare quale direzione punta l'asse z positivo puntando le dita del lato sinistro o destro nella direzione positiva della x e inserendole nella direzione positiva y. La direzione dei punti di controllo, verso o lontano da te, è la direzione che l'asse z positivo punta per il sistema di coordinate. Nella figura seguente vengono illustrati questi due sistemi di coordinate.

![illustrazione dei sistemi di coordinate cartesiane a sinistra e a destra](images/leftrght.png)

Direct3D usa un sistema di coordinate di sinistra. Se si trasferisce un'applicazione basata su un sistema di coordinate di destra, è necessario apportare due modifiche ai dati passati a Direct3D.

-   Capovolgere l'ordine dei vertici del triangolo in modo che il sistema li attraversi in senso orario dalla parte anteriore. In altre parole, se i vertici sono V0, V1, V2, passarli a Direct3D come V0, V2, V1.
-   Usare la matrice di visualizzazione per ridimensionare lo spazio globale di-1 nella direzione z. A tale scopo, capovolgere il segno del \_ membro 31, \_ 32, \_ 33 e \_ 34 della struttura [**D3DMATRIX**](d3dmatrix.md) usata per la matrice di visualizzazione.

Per ottenere gli importi a un mondo a destra, usare le funzioni [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) e [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) per definire la trasformazione di proiezione. Tuttavia, prestare attenzione a usare la funzione [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) corrispondente, invertire l'ordine di abbattimento delle backvisori e stendere il mapping del cubo di conseguenza.

Sebbene le coordinate di sinistra e di destra siano i sistemi più comuni, è disponibile un'ampia gamma di altri sistemi di coordinate usati nel software 3D. Ad esempio, non è insolito per le applicazioni di modellazione 3D usare un sistema di coordinate in cui l'asse y punta verso o lontano dal visualizzatore e l'asse z punta verso l'alto.

Formalmente, l'orientamento di un set di vettori di base (ad esempio un sistema di coordinate) può essere trovato dall'elaborazione del determinante della matrice definita dal particolare set di vettori di base. Se il determinante è positivo, la base è detta "positivamente" orientata (o a destra). Se il determinante è negativo, viene detto che la base è "negativamente" orientata (o a sinistra). Per una spiegazione del significato di un determinante, vedere qualsiasi risorsa di algebra lineare.

In modo informale, è possibile usare la "regola destra/sinistra" per determinare se un determinato set di vettori di base è costituito da un sistema di coordinate a destra o a sinistra.

Le operazioni essenziali eseguite su oggetti definiti in un sistema di coordinate 3D sono la conversione, la rotazione e il ridimensionamento. È possibile combinare queste trasformazioni di base per creare una matrice di trasformazione. Per informazioni dettagliate, vedere [trasformazioni (Direct3D 9)](transforms.md).

Quando si combinano queste operazioni, i risultati non sono commutativi. l'ordine in cui si moltiplicano le matrici è importante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistemi di coordinate e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



