---
description: 'In genere le applicazioni grafiche 3D usano due tipi di sistemi di coordinate cartesiani: mancino e destro.'
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: Sistemi di coordinate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e47b87ae6374d68b8c836dfb4818781e83e77c288f7bf05b121dbb4426c9aad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857577"
---
# <a name="coordinate-systems-direct3d-9"></a>Sistemi di coordinate (Direct3D 9)

In genere le applicazioni grafiche 3D usano due tipi di sistemi di coordinate cartesiani: mancino e destro. In entrambi i sistemi di coordinate, l'asse x positivo punta a destra e l'asse y positivo punta verso l'alto. È possibile ricordare la direzione dei punti positivi dell'asse z puntando le dita della mano sinistra o destra nella direzione x positiva e arricciandole nella direzione y positiva. La direzione in cui il cursore punta, verso o fuori dall'utente, è la direzione verso cui punta l'asse z positivo per il sistema di coordinate. La figura seguente mostra questi due sistemi di coordinate.

![illustrazione dei sistemi di coordinate cartesiani mancino e destro](images/leftrght.png)

Direct3D usa un sistema di coordinate mancino. Se si effettua il porting di un'applicazione basata su un sistema di coordinate destro, è necessario apportare due modifiche ai dati passati a Direct3D.

-   Capovolgere l'ordine dei vertici del triangolo in modo che il sistema li attraversi in senso orario dalla parte anteriore. In altre parole, se i vertici sono v0, v1, v2, passarli a Direct3D come v0, v2, v1.
-   Usare la matrice di visualizzazione per ridimensionare lo spazio globale di -1 nella direzione z. A tale scopo, capovolgere il segno dei \_ membri 31, \_ \_ 32, 33 e 34 della struttura \_ [**D3DMATRIX**](d3dmatrix.md) che si usa per la matrice di visualizzazione.

Per ottenere il valore di un mondo destro, usare le funzioni [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) e [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) per definire la trasformazione di proiezione. Prestare tuttavia attenzione a usare la funzione [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) corrispondente, invertire l'ordine di backface-culling e impostare il mapping del cubo di conseguenza.

Anche se le coordinate mancino e destro sono i sistemi più comuni, nel software 3D viene usata una varietà di altri sistemi di coordinate. Ad esempio, non è insolito che le applicazioni di modellazione 3D usino un sistema di coordinate in cui l'asse y punta verso o lontano dal visualizzatore e l'asse z punta verso l'alto.

Formalmente, l'orientamento di un set di vettori di base (ad esempio un sistema di coordinate) è reciso dal calcolo del determinante della matrice definita dal particolare set di vettori di base. Se il determinante è positivo, si dice che la base sia orientata "in modo positivo" (o destro). Se il determinante è negativo, si dice che la base sia orientata "negativamente" (o mancino). Per una spiegazione di che cos'è un determinante, vedere qualsiasi risorsa algebra lineare.

In modo informale, è possibile usare la "regola della mano destra/sinistra" per determinare se un determinato set di vettori di base forma un sistema di coordinate a destra o a sinistra.

Le operazioni essenziali eseguite sugli oggetti definiti in un sistema di coordinate 3D sono traslazione, rotazione e ridimensionamento. È possibile combinare queste trasformazioni di base per creare una matrice di trasformazione. Per informazioni dettagliate, [vedere Trasformazioni (Direct3D 9).](transforms.md)

Quando si combinano queste operazioni, i risultati non sono commutativi. l'ordine in cui si moltiplicano le matrici è importante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistemi di coordinate e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



