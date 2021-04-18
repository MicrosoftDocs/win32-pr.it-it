---
description: 'La classe CTransInPlaceFilter è progettata per i filtri di trasformazione sul posto, ovvero filtri che modificano i dati di input anziché copiare i dati tra i buffer. Per usare questa classe, derivare una nuova classe da CTransInPlaceFilter e implementare i metodi seguenti:'
ms.assetid: 3d6d5436-f280-4e36-96e4-40161e8115c2
title: Classe CTransInPlaceFilter (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f59dd312adbb95797caf695aecea082f296df5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330839"
---
# <a name="ctransinplacefilter-class"></a>Classe CTransInPlaceFilter

![gerarchia di classi ctransinplacefilter](images/tsip03.png)

La `CTransInPlaceFilter` classe è progettata per i filtri di trasformazione sul posto, ovvero filtri che modificano i dati di input anziché copiare i dati tra i buffer. Per usare questa classe, derivare una nuova classe da `CTransInPlaceFilter` e implementare i metodi seguenti:

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransInPlaceFilter:: Transform**](ctransinplacefilter-transform.md)

Questa classe usa la classe [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) per il pin di input e la classe [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) per il pin di output. In genere, non è necessario eseguire l'override di queste classi pin. Il filtro crea entrambi i pin nel metodo [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) . Se si esegue l'override delle classi pin, è necessario eseguire l'override di **GetPin** per creare i pin personalizzati.

Questa classe è progettata in modo che il tipo di input corrisponda sempre al tipo di output. Quando possibile, il filtro usa un solo allocatore per entrambe le connessioni pin.

## <a name="preferred-media-types"></a>Tipi di supporti preferiti

Se il pin di output è già connesso, il pin di input offre i tipi preferiti del filtro downstream. In realtà restituisce semplicemente l'oggetto enumeratore del filtro downstream. In caso contrario, non ha tipi preferiti. Il pin di output ha lo stesso comportamento, ma in senso inverso: se il pin di input è già connesso, il pin di output offre i tipi preferiti del filtro upstream. In caso contrario, non ha tipi preferiti

## <a name="pin-connections"></a>Connessioni pin

Quando un pin si connette, il filtro in genere riconnette l'altro pin, per assicurarsi che entrambi i pin usino lo stesso tipo di supporto e lo stesso allocatore. Il meccanismo per la riconnessione dei pin è descritto in [riconnessione di pin](reconnecting-pins.md). Sono possibili due scenari: il pin di input si connette per primo o il pin di output si connette per primo.

Si supponga che il pin di input si connetta per primo. Si verificano i passaggi seguenti:

1.  Il pin di input chiama il metodo [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per verificare il tipo di supporto.
2.  Il filtro upstream seleziona un allocatore. A questo punto, il pin di input non ha requisiti per l'allocatore e accetta qualsiasi allocatore per la connessione. Se il filtro upstream richiede un allocatore, il pin ne crea uno nuovo. Per i motivi descritti a breve, questo allocatore non verrà utilizzato nella connessione finale. Viene fornito solo per aiutare a completare questa fase del processo di connessione.

In seguito, quando il pin di output si connette:

1.  Il pin di output chiama il metodo [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per verificare il tipo di supporto. Chiama anche [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul filtro upstream. In questo modo si garantisce che il pin di input possa modificare il tipo di supporto corrispondente.
2.  Il pin di output chiama il metodo [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per verificare il tipo di supporto. Chiama anche [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul filtro upstream. In questo modo si garantisce che il pin di input possa modificare il tipo di supporto corrispondente.
3.  Il pin di output chiama il metodo [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per verificare il tipo di supporto. Chiama anche [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul filtro upstream. In questo modo si garantisce che il pin di input possa modificare il tipo di supporto corrispondente.
4.  Questa volta, il metodo [**Getallocator**](ctransinplaceinputpin-getallocator.md) del PIN di input restituisce l'allocatore downstream e [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) restituisce i requisiti dell'allocatore del filtro downstream. Il pin di input accetta qualsiasi allocatore scelto dal filtro upstream.
5.  Questa volta, il metodo [**Getallocator**](ctransinplaceinputpin-getallocator.md) del PIN di input restituisce l'allocatore downstream e [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) restituisce i requisiti dell'allocatore del filtro downstream. Il pin di input accetta qualsiasi allocatore scelto dal filtro upstream.

Si consideri ora lo scenario opposto, in cui il pin di output è il primo pin per la connessione.

1.  Il pin di output chiama il metodo [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro per verificare il tipo di supporto.
2.  Viene selezionato un allocatore, che fa riferimento all'uso dell'allocatore del filtro downstream.

Quindi, quando il pin di input si connette:

1.  Il pin di input controlla il tipo di supporto chiamando [**CheckInputType**](ctransformfilter-checkinputtype.md) sul filtro e chiamando [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sul pin di output del filtro downstream.
2.  Se il tipo di input non corrisponde al tipo di output, il filtro riconnette il pin di output.
3.  Il filtro upstream seleziona un allocatore. Il metodo [**Getallocator**](ctransinplaceinputpin-getallocator.md) del PIN di input restituisce l'allocatore downstream e il pin di input accetta qualsiasi allocatore selezionato dal filtro upstream.
4.  Il filtro usa lo stesso allocatore per la connessione downstream, probabilmente sostituendo l'allocatore downstream originale.

Questa sequenza di eventi cambia leggermente se uno degli allocatori interessati è di sola lettura, perché l'allocatore downstream deve essere scrivibile. In tal caso, il filtro può utilizzare due allocatori distinti.

Per ulteriori informazioni sull'utilizzo di questa classe, vedere la pagina relativa alla [scrittura di filtri di trasformazione](writing-transform-filters.md).



| Variabili membro protette                                                        | Descrizione                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**\_bModifiesData m**](ctransinplacefilter-m-bmodifiesdata.md)                   | Indica se il filtro modifica i dati di esempio.                           |
| Metodi protetti                                                                 | Descrizione                                                                      |
| [**Copia**](ctransinplacefilter-copy.md)                                          | Copia un esempio di supporto.                                                           |
| [**InputPin**](ctransinplacefilter-inputpin.md)                                  | Recupera un puntatore al pin di input del filtro.                                   |
| [**OutputPin**](ctransinplacefilter-outputpin.md)                                | Recupera un puntatore al pin di output del filtro.                                  |
| [**TypesMatch**](ctransinplacefilter-typesmatch.md)                              | Determina se il tipo di supporto di input corrisponde al tipo di supporto di output.           |
| [**UsingDifferentAllocators**](ctransinplacefilter--usingdifferentallocators.md) | Determina se i pin di input e di output utilizzano allocatori diversi.     |
| Metodi pubblici                                                                    | Descrizione                                                                      |
| [**CTransInPlaceFilter**](ctransinplacefilter-ctransinplacefilter.md)            | Metodo del costruttore.                                                              |
| [**GetPin**](ctransinplacefilter-getpin.md)                                      | Recupera un PIN.                                                                 |
| [**GetMediaType**](ctransinplacefilter-getmediatype.md)                          | Recupera un tipo di supporto preferito per il pin di output.                             |
| [**DecideBufferSize**](ctransinplacefilter-decidebuffersize.md)                  | Imposta i requisiti del buffer del PIN di output.                                       |
| [**CheckTransform**](ctransinplacefilter-checktransform.md)                      | Verifica se un tipo di supporto di input è compatibile con un tipo di supporto di output.      |
| [**CompleteConnect**](ctransinplacefilter-completeconnect.md)                    | Completa una connessione pin.                                                      |
| [**Ricevere**](ctransinplacefilter-receive.md)                                    | Riceve un esempio multimediale, lo elabora e lo recapita al filtro downstream. |
| Metodi virtuali puri                                                              | Descrizione                                                                      |
| [**Transform**](ctransinplacefilter-transform.md)                                | Trasforma un campione sul posto.                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




