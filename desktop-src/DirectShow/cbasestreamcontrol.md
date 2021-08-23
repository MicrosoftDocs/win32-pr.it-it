---
description: Questa classe implementa l'interfaccia IAMStreamControl per i pin di input e output.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: Classe CBaseStreamControl (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eb1d8d747d88a416792d59af79af41c047cb51aa61688aef9d6b105790bbae8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157204"
---
# <a name="cbasestreamcontrol-class"></a>Classe CBaseStreamControl

![Gerarchia di classi cbasestreamcontrol](images/strmctl1.png)

Questa classe implementa [**l'interfaccia IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) per i pin di input e output. Fornisce il controllo sull'avvio e l'arresto di un singolo pin sul filtro. Un pin che supporta **IAMStreamControl** deve ereditare da questa classe di base. Di seguito è riportata una dichiarazione tipica per un pin di input:

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

Assicurarsi di eseguire l'override **di NonDelegatingQueryInteface per** esporre **IAMStreamControl**. Per altre informazioni, vedere [Come implementare IUnknown.](how-to-implement-iunknown.md)



| Metodi pubblici                                                        | Descrizione                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**CBaseStreamControl**](cbasestreamcontrol-cbasestreamcontrol.md)   | Metodo del costruttore.                                                                                  |
| [**~CBaseStreamControl**](cbasestreamcontrol--cbasestreamcontrol.md) | Metodo del distruttore.                                                                                   |
| [**CheckStreamState**](cbasestreamcontrol-checkstreamstate.md)       | Determina se un campione di supporti deve essere recapitato o eliminato.                                  |
| [**Flushing**](cbasestreamcontrol-flushing.md)                       | Notifica alla classe di base che il pin è stato avviato o interrotto.                                |
| [**NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md)     | Notifica al pin quando cambia lo stato del filtro.                                                    |
| [**SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md)           | Specifica il sink di evento per gli eventi di controllo del flusso.                                                  |
| [**SetSyncSource**](cbasestreamcontrol-setsyncsource.md)             | Notifica alla classe di base dell'orologio di riferimento corrente.                                              |
| Metodi di IAMStreamControl                                              | Descrizione                                                                                          |
| [**GetInfo**](cbasestreamcontrol-getinfo.md)                         | Recupera informazioni sulle impostazioni correnti del controllo di flusso, inclusi gli orari di inizio e arresto. |
| [**StartAt**](cbasestreamcontrol-startat.md)                         | Indica al pin quando iniziare a recapitare i dati.                                                       |
| [**Stopat**](cbasestreamcontrol-stopat.md)                           | Indica al pin quando interrompere la distribuzione dei dati.                                                        |



 

## <a name="remarks"></a>Commenti

Questa classe richiede il segnaposto e il filtro proprietario per notificare alla classe quando si verificano vari eventi, ad esempio il filtro che unisce il grafico o riceve un nuovo clock di riferimento. È necessario chiamare i metodi della classe seguenti:

-   Nel metodo [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) del filtro chiamare il metodo [**CBaseStreamControl::SetSyncSource.**](cbasestreamcontrol-setsyncsource.md) Questo metodo notifica la classe dell'orologio di riferimento corrente.
-   Nel metodo [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) del filtro chiamare il metodo [**CBaseStreamControl::SetFilterGraph.**](cbasestreamcontrol-setfiltergraph.md) Questo metodo fornisce alla classe un puntatore a Filter Graph Manager, in modo che la classe possa inviare gli eventi di controllo del flusso.
-   Ogni volta che lo stato del filtro cambia (in esecuzione, sospeso o arrestato), chiamare il metodo [**CBaseStreamControl::NotifyFilterState.**](cbasestreamcontrol-notifyfilterstate.md)
-   Nei metodi [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) del pin chiamare il metodo [**CBaseStreamControl::Flushing.**](cbasestreamcontrol-flushing.md)

La classe usa l'orologio di riferimento del grafico dei filtri per determinare quali campioni devono essere recapitati dal filtro e `CBaseStreamControl` quali deve essere eliminato. Nel metodo [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del pin chiamare il metodo [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) con un puntatore all'esempio multimediale in ingresso. Se il metodo restituisce il valore STREAM \_ FLOWING, recapitare l'esempio a valle. In caso contrario, ignorarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




