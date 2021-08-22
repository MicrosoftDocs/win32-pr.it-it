---
description: Sempre più spesso, le applicazioni utilizzano effetti speciali comunemente usati nei film e nei video, ad esempio dissolvenze, scorrimenti e dissolvenze.
ms.assetid: 6203922f-9594-4e5c-9baa-8b27ac30978f
title: Dissolvenza, dissolvenza e scorrimento rapido (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d6df834ad19fa4b00b6e4706d0884227bc4af33c6a25ec09cba14757e1248
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607461"
---
# <a name="dissolves-fades-and-swipes-direct3d-9"></a>Dissolvenza, dissolvenza e scorrimento rapido (Direct3D 9)

Sempre più spesso, le applicazioni utilizzano effetti speciali comunemente usati nei film e nei video, ad esempio dissolvenze, scorrimenti e dissolvenze.

In una dissolvenza, un'immagine viene gradualmente sostituita da un'altra in una sequenza uniforme di fotogrammi. Anche se Direct3D fornisce metodi per l'uso della fusione di più trame per ottenere lo stesso effetto, le applicazioni che usano il buffer di stencil per le dissolvenze possono usare funzionalità di fusione trame per altri effetti durante la dissolvenza.

Quando l'applicazione esegue una dissolvenza, deve eseguire il rendering di due immagini diverse. Usa il buffer di stencil per controllare quali pixel di ogni immagine vengono disegnati sulla superficie di destinazione del rendering. È possibile definire una serie di maschere di stencil e copiarle nel buffer degli stencil nei fotogrammi successivi. In alternativa, è possibile definire una maschera di stencil di base per il primo frame e modificarla in modo incrementale.

All'inizio della dissolvenza, l'applicazione imposta la funzione di stencil e la maschera di stencil in modo che la maggior parte dei pixel dell'immagine iniziale superi il test dello stencil. La maggior parte dei pixel dell'immagine finale dovrebbe non riuscire nel test dello stencil. Nei fotogrammi successivi, la maschera di stencil viene aggiornata in modo che un numero sempre minore di pixel nell'immagine iniziale superi il test. Con l'avanzamento dei fotogrammi, il test ha esito negativo per un numero sempre minore di pixel nell'immagine finale. In questo modo, l'applicazione può eseguire una dissolvenza usando qualsiasi modello di dissolvenza arbitrario.

La dissolversi o dissolversi è un caso speciale di dissoluzione. Quando si dissolve, il buffer di stencil viene usato per dissolvere da un'immagine nera o bianca a un rendering di una scena 3D. La dissolvenza è l'opposto, l'applicazione inizia con il rendering di una scena 3D e si dissolve in bianco o nero. La dissolvenza può essere eseguita usando qualsiasi modello arbitrario che si vuole usare.

Le applicazioni Direct3D usano una tecnica simile per lo scorrimento rapido. Ad esempio, quando un'applicazione esegue uno scorrimento da sinistra a destra, l'immagine finale appare scorrere gradualmente sopra l'immagine iniziale da sinistra a destra. Come in una dissolvenza, è necessario definire una serie di maschere di stencil caricate nel buffer degli stencil nei frame successivi oppure modificare in seguito la maschera di stencil iniziale. Le maschere di stencil vengono usate per disabilitare la scrittura di pixel dall'immagine iniziale e per abilitare la scrittura di pixel dall'immagine finale.

Uno scorrimento rapido è un po' più complesso di una dissolvenza in quanto l'applicazione deve leggere i pixel dall'immagine finale nell'ordine inverso dello scorrimento. In altre informazioni, se lo scorrimento rapido si sposta da sinistra a destra, l'applicazione deve leggere i pixel dall'immagine finale da destra a sinistra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche di buffer di stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



