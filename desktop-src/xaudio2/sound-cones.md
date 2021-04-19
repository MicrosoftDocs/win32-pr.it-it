---
description: Modello che descrive la sonorità del suono orientato.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Coni audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317844"
---
# <a name="sound-cones"></a>Coni audio

Modello che descrive la sonorità del suono orientato.

Un suono senza orientamento ha la stessa ampiezza a una distanza specificata in tutte le direzioni. Un suono con orientamento è più forte nella direzione dell'orientamento. Il modello che descrive la sonorità del suono orientato è detto cono acustico. I coni acustici sono costituiti da un cono interno (o interno) e da un cono esterno (o esterno). L'angolo del cono esterno deve essere sempre uguale o maggiore dell'angolo del cono interno.

In qualsiasi angolo all'interno del cono interno, il volume del suono viene impostato sul volume del cono interno. In questo modo viene preso in considerazione il volume di base del buffer, la distanza dal listener, l'orientamento del listener se il listener ha un cono e così via.

In qualsiasi angolo esterno al cono esterno, il volume normale viene attenuato da un fattore impostato dall'applicazione. Il livello del volume del cono esterno è espresso come scaler di ampiezza lineare: 1,0 f non rappresenta alcuna attenuazione applicata al segnale originale, 0,5 f denota un'attenuazione di 6 dB e 0,0 f risultano silenziosi. È consentita anche l'amplificazione (volume > 1,0 f) e non è stato bloccato. L'intervallo di volumi validi è effettivamente 0,0 f a 2,0 f.

Tra i coni interni ed esterni è presente una zona di transizione dal volume interno al volume esterno. Il volume si avvicina al volume esterno del cono Man mano che aumenta l'angolo.

I coni possono influenzare parametri diversi dal volume. Anche il livello di filtro di passaggio basso e di invio del riverbero potrebbe essere influenzato, rendendo la tecnica ancora più drammatica. Ad esempio, con un cono sul listener, è possibile specificare che tutti i suoni dietro il listener ottengano un bit smorzato e abbiano un contenuto leggermente più alto per il rapporto tra reverbi diretti. Che forniscono più segnali che il suono è dietro l'utente. Ciò migliora il realismo.

Nella figura seguente viene illustrato il concetto di coni audio.

![coni audio](images/common-audio-concepts-sound-cones.png)

La progettazione corretta dei coni audio può aggiungere effetti significativi all'applicazione. Ad esempio, è possibile posizionare una sorgente audio al centro di una stanza, impostando l'orientamento verso una porta aperta in un corridoio. Impostare quindi l'angolo del cono interno in modo che si estenda alla larghezza della porta, rendere il cono esterno a un bit più ampio e infine impostare il volume del cono esterno su impercettibile. Un listener che si muove lungo il corridoio inizierà a udire il suono solo quando è vicino alla porta. Il suono sarà più forte quando il listener passa davanti alla porta aperta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti audio comuni](common-audio-concepts.md)
</dt> <dt>

[X3DAudio](x3daudio-overview.md)
</dt> <dt>

[**\_Cono X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



