---
description: Passaggio 3.
ms.assetid: b2b5dafc-d38d-4ec3-a390-55229495b4f9
title: Passaggio 3. Negoziazione del tipo di supporto multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3ff8539d0d7de2c9b7300ddb90ad86ca471710
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103885982"
---
# <a name="step-3-support-media-type-negotiation"></a>Passaggio 3. Negoziazione del tipo di supporto multimediale

Questo è il passaggio 3 dell'esercitazione [scrittura dei filtri di trasformazione](writing-transform-filters.md).

Quando due pin si connettono, devono accordarsi su un tipo di supporto per la connessione. Il tipo di supporto descrive il formato dei dati. Senza il tipo di supporto, un filtro potrebbe fornire un tipo di dati, ma solo un altro filtro può considerarlo come un altro elemento.

Il meccanismo di base per negoziare i tipi di supporto è il metodo [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) . Il pin di output chiama questo metodo sul pin di input con un tipo di supporto proposto. Il pin di input accetta la connessione o lo rifiuta. Se la connessione viene rifiutata, il pin di output può provare un altro tipo di supporto. Se non vengono trovati tipi appropriati, la connessione ha esito negativo. Facoltativamente, il pin di input può annunciare un elenco di tipi che preferisce, tramite il metodo [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) . Il pin di output può utilizzare questo elenco quando propone i tipi di supporto, sebbene non sia necessario.

La classe **CTransformFilter** implementa un framework generale per questo processo, come indicato di seguito:

-   Il pin di input non ha tipi di supporti preferiti. Si basa interamente sul filtro upstream per proporre il tipo di supporto. Per i dati video, questa operazione è sensata, perché il tipo di supporto include le dimensioni dell'immagine e la frequenza dei fotogrammi. In genere, tali informazioni devono essere fornite da un filtro dell'origine upstream o da un filtro parser. Nel caso dei dati audio, il set di formati possibili è più piccolo, quindi può essere utile per il pin di input offrire alcuni tipi preferiti. In tal caso, eseguire l'override di [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) sul pin di input.
-   Quando il filtro upstream propone un tipo di supporto, il pin di input chiama il metodo [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) , che accetta o rifiuta il tipo.
-   Il pin di output non verrà connesso, a meno che il pin di input non sia connesso per primo. Questo comportamento è tipico per i filtri di trasformazione. Nella maggior parte dei casi, il filtro deve determinare il tipo di input prima di poter impostare il tipo di output.
-   Quando il pin di output si connette, dispone di un elenco di tipi di supporti che propone al filtro downstream. Chiama il metodo [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) per generare l'elenco. Il pin di output tenterà anche qualsiasi tipo di supporto proposto dal filtro downstream.
-   Per verificare se un particolare tipo di output è compatibile con il tipo di input, il pin di output chiama il metodo [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .

I tre metodi **CTransformFilter** elencati in precedenza sono metodi virtuali puri, quindi la classe derivata deve implementarli. Nessuno di questi metodi appartiene a un'interfaccia COM; sono semplicemente parte dell'implementazione fornita dalle classi base.

Le sezioni seguenti descrivono ogni metodo in modo più dettagliato:

-   [Passaggio 3A. Implementare il metodo CheckInputType](step-3a--implement-the-checkinputtype-method.md)
-   [Passaggio 3B. Implementare il metodo GetMediaType](step-3b--implement-the-getmediatype-method.md)
-   [Passaggio 3C. Implementare il metodo CheckTransform](step-3c--implement-the-checktransform-method.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di connessione dei filtri](how-filters-connect.md)
</dt> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



