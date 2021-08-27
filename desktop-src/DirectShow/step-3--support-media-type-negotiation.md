---
description: Implementare il supporto per la negoziazione del tipo di supporto come parte della scrittura di un filtro di trasformazione. Il tipo di supporto descrive il formato dei dati.
ms.assetid: b2b5dafc-d38d-4ec3-a390-55229495b4f9
title: Passaggio 3. Supportare la negoziazione del tipo di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1558d5b1a7fd9db41fef7e5a9818d93c306f4f15f42099d4cb88f66b34725660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051471"
---
# <a name="step-3-support-media-type-negotiation"></a>Passaggio 3. Supportare la negoziazione del tipo di supporto

Questo è il passaggio 3 dell'esercitazione [Scrittura di filtri di trasformazione](writing-transform-filters.md).

Quando si connettono due pin, devono accettare un tipo di supporto per la connessione. Il tipo di supporto descrive il formato dei dati. Senza il tipo di supporto, un filtro potrebbe recapitare un tipo di dati, solo per fare in modo che un altro filtro lo tratti come un altro.

Il meccanismo di base per negoziare i tipi di supporti [**è il metodo IPin::ReceiveConnection.**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) Il pin di output chiama questo metodo sul pin di input con un tipo di supporto proposto. Il pin di input accetta la connessione o la rifiuta. Se rifiuta la connessione, il pin di output può provare un altro tipo di supporto. Se non vengono trovati tipi adatti, la connessione non riesce. Facoltativamente, il pin di input può annunciare un elenco di tipi che preferisce, tramite il [**metodo IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) Il pin di output può usare questo elenco quando propone tipi di supporti, anche se non è necessario.

La **classe CTransformFilter** implementa un framework generale per questo processo, come indicato di seguito:

-   Il pin di input non ha tipi di supporti preferiti. Si basa interamente sul filtro upstream per proporre il tipo di supporto. Per i dati video, ciò ha senso, perché il tipo di supporto include le dimensioni dell'immagine e la frequenza dei fotogrammi. In genere, tali informazioni devono essere fornite da un filtro di origine upstream o da un filtro del parser. Nel caso dei dati audio, il set di formati possibili è più piccolo, quindi può essere pratico per il pin di input offrire alcuni tipi preferiti. In tal caso, eseguire l'override [**di CBasePin::GetMediaType**](cbasepin-getmediatype.md) sul pin di input.
-   Quando il filtro upstream propone un tipo di supporto, il pin di input chiama il metodo [**CTransformFilter::CheckInputType,**](ctransformfilter-checkinputtype.md) che accetta o rifiuta il tipo.
-   Il pin di output non si connetterà a meno che il pin di input non sia connesso per primo. Questo comportamento è tipico per i filtri di trasformazione. Nella maggior parte dei casi, il filtro deve determinare il tipo di input prima di poter impostare il tipo di output.
-   Quando il pin di output si connette, ha un elenco di tipi di supporti che propone al filtro downstream. Chiama il [**metodo CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) per generare questo elenco. Il pin di output proverà anche tutti i tipi di supporti proposti dal filtro downstream.
-   Per verificare se un determinato tipo di output è compatibile con il tipo di input, il pin di output chiama il metodo [**CTransformFilter::CheckTransform.**](ctransformfilter-checktransform.md)

I tre **metodi CTransformFilter** elencati in precedenza sono metodi virtuali puri, pertanto la classe derivata deve implementarli. Nessuno di questi metodi appartiene a un'interfaccia COM. fanno semplicemente parte dell'implementazione fornita dalle classi di base.

Le sezioni seguenti descrivono ogni metodo in modo più dettagliato:

-   [Passaggio 3A. Implementare il metodo CheckInputType](step-3a--implement-the-checkinputtype-method.md)
-   [Passaggio 3B. Implementare il metodo GetMediaType](step-3b--implement-the-getmediatype-method.md)
-   [Passaggio 3C. Implementare il metodo CheckTransform](step-3c--implement-the-checktransform-method.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di Connessione](how-filters-connect.md)
</dt> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



