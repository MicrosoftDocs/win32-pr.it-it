---
description: Modello che descrive il volume del suono orientato.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Coni sonori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc6b55ce1cc98b1875dff7079a0a304ef77c5567966808a4678f01f2297ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005776"
---
# <a name="sound-cones"></a>Coni sonori

Modello che descrive il volume del suono orientato.

Un suono senza orientamento ha la stessa ampiezza a una determinata distanza in tutte le direzioni. Un suono con orientamento è più alto nella direzione dell'orientamento. Il modello che descrive il volume del suono orientato è detto cono sonoro. I coni sonori sono costituito da un cono interno (o interno) e da un cono esterno (o esterno). L'angolo esterno del cono deve essere sempre uguale o maggiore dell'angolo interno del cono.

In qualsiasi angolo all'interno del cono interno, il volume del suono viene impostato sul volume interno del cono. Questo prende in considerazione il volume di base del buffer, la distanza dal listener, l'orientamento del listener se il listener ha un proprio cono e così via.

In qualsiasi angolo esterno al cono esterno, il volume normale viene attenuato da un fattore impostato dall'applicazione. Il livello del volume esterno del cono è espresso come scalatore di ampiezza lineare: 1,0 f non rappresenta alcuna attenuazione applicata al segnale originale, 0,5 f indica un'attenuazione di 6 dB e 0,0 f risulta in silenzio. Anche l'amplificazione (volume > 1,0 f) è consentita e non è ancorata. L'intervallo di volumi valido è effettivamente compreso tra 0,0 f e 2,0 f.

Tra i coni interni ed esterni è una zona di transizione dal volume interno al volume esterno. Il volume si avvicina al volume esterno del cono all'aumentare dell'angolo.

I coni possono influire sui parametri diversi dal volume. Anche il livello di trasmissione del riverbero e del filtro pass basso può essere influenzato, rendendo la tecnica ancora più drastica. Ad esempio, con un cono sul listener, è possibile specificare tutti i suoni dietro il listener ottenere un po 'ovattati e hanno un contenuto leggermente più alto del rapporto riverbero-diretto. Questi forniscono più segnali che il suono è dietro l'utente. Questo migliora il realismo.

La figura seguente illustra il concetto di coni sonori.

![coni sonori](images/common-audio-concepts-sound-cones.png)

La corretta progettazione dei coni sonori può aggiungere effetti notevoli all'applicazione. Ad esempio, è possibile posizionare una sorgente sonora al centro di una stanza, impostandone l'orientamento verso una porta aperta in un ingresso. Impostare quindi l'angolo del cono interno in modo che si estenda alla larghezza della porta, rendere il cono esterno un po' più ampio e infine impostare il volume del cono esterno su inaudibile. Un listener che si sposta lungo il ingresso inizierà a udire il suono solo quando si trova vicino alla porta. Il suono sarà più forte quando l'ascoltatore passa davanti alla porta aperta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti comuni relativi all'audio](common-audio-concepts.md)
</dt> <dt>

[X3DAudio](x3daudio-overview.md)
</dt> <dt>

[**CONO X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



