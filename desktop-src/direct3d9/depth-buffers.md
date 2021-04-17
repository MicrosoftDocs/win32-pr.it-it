---
description: Un buffer di profondità, spesso denominato buffer z o w-buffer, è una proprietà del dispositivo che archivia le informazioni di profondità che devono essere usate da Direct3D.
ms.assetid: vs|directx_sdk|~\depth_buffers.htm
title: Buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1ab41ba98ca5e3b08980ac90a572a19fc8a72a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481549"
---
# <a name="depth-buffers-direct3d-9"></a>Buffer di profondità (Direct3D 9)

Un buffer di profondità, spesso denominato buffer z o w-buffer, è una proprietà del dispositivo che archivia le informazioni di profondità che devono essere usate da Direct3D. Quando Direct3D esegue il rendering di una scena in una superficie di destinazione, può usare la memoria in una superficie del buffer di profondità associata come area di lavoro per determinare il modo in cui i pixel dei poligoni rasterizzati occludere l'uno all'altro. Direct3D usa una superficie Direct3D fuori schermo come destinazione in cui vengono scritti i valori dei colori finali. La superficie del buffer di profondità associata alla superficie di destinazione di rendering viene utilizzata per archiviare informazioni di profondità che indicano a Direct3D il livello di profondità di ogni pixel visibile nella scena.

Quando una scena viene rasterizzata con il buffering di profondità abilitato, viene testato ogni punto della superficie di rendering. I valori nel buffer di profondità possono essere una coordinata z di un punto o la relativa coordinata w uniforme, dalla posizione del punto (x, y, z, w) nello spazio di proiezione. Un buffer di profondità che usa i valori z è spesso definito un buffer z e uno che usa i valori w viene definito w-buffer. Ogni tipo di buffer di profondità presenta vantaggi e svantaggi, descritti più avanti.

All'inizio del test, il valore di profondità nel buffer di profondità viene impostato sul valore massimo possibile per la scena. Il valore del colore sulla superficie di rendering è impostato sul valore del colore di sfondo o sul valore del colore della trama di sfondo in quel punto. Ogni poligono nella scena viene testato per verificare se si interseca con la coordinata corrente (x, y) sulla superficie di rendering. In caso contrario, il valore di profondità, che sarà la coordinata z in un buffer z, e la coordinata w in un w-buffer, nel punto corrente viene testato per verificare se è più piccolo del valore di profondità archiviato nel buffer di profondità. Se la profondità del valore del poligono è inferiore, viene archiviata nel buffer di profondità e il valore del colore del poligono viene scritto nel punto corrente sulla superficie di rendering. Se il valore di profondità del poligono a quel punto è maggiore, viene testato il poligono successivo nell'elenco. Questo processo è illustrato nella figura seguente.

![diagramma dei valori di profondità del test](images/zbuffer.png)

> [!Note]  
> Anche se la maggior parte delle applicazioni non usa questa funzionalità, è possibile modificare il confronto usato da Direct3D per determinare quali valori vengono inseriti nel buffer di profondità e successivamente la superficie di destinazione di rendering. A tale scopo, modificare il valore dello stato di \_ rendering ZFUNC di D3DRS. In alcuni componenti hardware, la modifica della funzione compare può disabilitare il test gerarchico z.

 

Quasi tutti gli acceleratori sul mercato supportano il buffering z, rendendo attualmente il buffer z il tipo più comune di buffer di profondità. I buffer z, tuttavia, presentano svantaggi. A causa della matematica, i valori z generati in un buffer z tendono a non essere distribuiti in modo uniforme nell'intervallo del buffer z (in genere da 0,0 a 1,0, inclusi). In particolare, il rapporto tra i piani di ritaglio lontani e vicini influiscono fortemente sul modo in cui i valori z vengono distribuiti in modo non uniforme. Se si utilizza un rapporto distanza dal piano esterno a distanza quasi dal piano di 100, il 90% dell'intervallo di buffer di profondità viene impiegato per il primo 10% dell'intervallo di profondità della scena. Le applicazioni tipiche per le simulazioni visive o di intrattenimento con scenari esterni richiedono spesso rapporti di tipo piano/vicino a un piano di distanza compreso tra 1.000 e 10.000. Con un rapporto di 1.000, il 98% dell'intervallo viene impiegato per il primo 2% dell'intervallo di profondità e la distribuzione diventa peggiore con rapporti più elevati. Ciò può causare l'inserimento di elementi di superficie nascosti in oggetti distanti, soprattutto quando si usano buffer di profondità a 16 bit, la più comunemente supportata profondità di bit.

Un buffer di profondità basato su w, d'altra parte, è spesso distribuito in modo più uniforme tra i piani di ritaglio vicini e lontani rispetto a un buffer z. Il vantaggio principale è che il rapporto tra le distanze per i piani di ritaglio lontani e vicini non è più un problema. Questo consente alle applicazioni di supportare intervalli massimi elevati, ottenendo al tempo stesso un buffer di profondità relativamente accurato vicino al punto d'occhio. Un buffer di profondità basato su w non è perfetto e talvolta può presentare elementi della superficie nascosta per oggetti near. Un altro svantaggio dell'approccio con buffer w è correlato al supporto hardware: w-buffering non è supportato con l'hardware come il buffer z.

L'uso di un buffer z richiede un sovraccarico durante il rendering. È possibile utilizzare varie tecniche per ottimizzare il rendering quando si utilizzano i buffer z. Per informazioni dettagliate, vedere [prestazioni del buffer Z](performance-optimizations.md).

> [!Note]  
> L'interpretazione effettiva di un valore di profondità è specifica per il renderer.

 

Questa sezione presenta informazioni sull'uso dei buffer di profondità per la rimozione della linea nascosta e della superficie nascosta.

-   [Esecuzione di query per il supporto del buffer di profondità (Direct3D 9)](querying-for-depth-buffer-support.md)
-   [Creazione di un buffer di profondità (Direct3D 9)](creating-a-depth-buffer.md)
-   [Abilitazione del buffer di profondità (Direct3D 9)](enabling-depth-buffering.md)
-   [Recupero di un buffer di profondità (Direct3D 9)](retrieving-a-depth-buffer.md)
-   [Cancellazione dei buffer di profondità (Direct3D 9)](clearing-depth-buffers.md)
-   [Modifica dell'accesso in scrittura al buffer di profondità (Direct3D 9)](changing-depth-buffer-write-access.md)
-   [Modifica delle funzioni di confronto del buffer di profondità (Direct3D 9)](changing-depth-buffer-comparison-functions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



