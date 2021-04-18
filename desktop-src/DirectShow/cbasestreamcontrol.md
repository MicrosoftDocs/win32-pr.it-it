---
description: Questa classe implementa l'interfaccia IAMStreamControl per i pin di input e di output.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: Classe CBaseStreamControl (Strmctl. h)
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
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326937"
---
# <a name="cbasestreamcontrol-class"></a>Classe CBaseStreamControl

![gerarchia di classi cbasestreamcontrol](images/strmctl1.png)

Questa classe implementa l'interfaccia [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) per i pin di input e di output. Consente di controllare l'avvio e l'arresto di un singolo pin sul filtro. Un pin che supporta **IAMStreamControl** deve ereditare da questa classe di base. Di seguito è riportata una dichiarazione tipica per un pin di input:

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

Assicurarsi di eseguire l'override di **NonDelegatingQueryInteface** per esporre **IAMStreamControl**. Per ulteriori informazioni, vedere [How to implement IUnknown](how-to-implement-iunknown.md).



| Metodi pubblici                                                        | Descrizione                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**CBaseStreamControl**](cbasestreamcontrol-cbasestreamcontrol.md)   | Metodo del costruttore.                                                                                  |
| [**~ CBaseStreamControl**](cbasestreamcontrol--cbasestreamcontrol.md) | Metodo del distruttore.                                                                                   |
| [**CheckStreamState**](cbasestreamcontrol-checkstreamstate.md)       | Determina se un campione multimediale deve essere recapitato o rimosso.                                  |
| [**Flushing**](cbasestreamcontrol-flushing.md)                       | Notifica alla classe di base che il pin ha avviato o interrotto lo svuotamento.                                |
| [**NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md)     | Notifica al pin quando lo stato del filtro viene modificato.                                                    |
| [**SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md)           | Specifica il sink di evento per gli eventi di controllo di flusso.                                                  |
| [**SetSyncSource**](cbasestreamcontrol-setsyncsource.md)             | Notifica alla classe di base l'orologio di riferimento corrente.                                              |
| Metodi IAMStreamControl                                              | Descrizione                                                                                          |
| [**GetInfo**](cbasestreamcontrol-getinfo.md)                         | Recupera le informazioni sulle impostazioni correnti del controllo del flusso, incluse le ore di inizio e di fine. |
| [**StartAt**](cbasestreamcontrol-startat.md)                         | Informa il PIN quando iniziare a consegnare i dati.                                                       |
| [**StopAt**](cbasestreamcontrol-stopat.md)                           | Informa il PIN quando interrompere la distribuzione dei dati.                                                        |



 

## <a name="remarks"></a>Commenti

Questa classe richiede il PIN e il filtro proprietario per notificare alla classe quando si verificano vari eventi, ad esempio il filtro che aggiunge il grafo o riceve un nuovo Clock di riferimento. È necessario chiamare i metodi della classe seguenti:

-   Nel metodo [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) del filtro chiamare il metodo [**CBaseStreamControl:: SetSyncSource**](cbasestreamcontrol-setsyncsource.md) . Questo metodo notifica alla classe l'orologio di riferimento corrente.
-   Nel metodo [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) del filtro chiamare il metodo [**CBaseStreamControl:: SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) . Questo metodo assegna alla classe un puntatore al gestore del grafico dei filtri, in modo che la classe possa inviare gli eventi di controllo di flusso corretti.
-   Ogni volta che il filtro cambia stato (in esecuzione, in pausa o arrestato), chiamare il metodo [**CBaseStreamControl:: NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) .
-   Nei metodi [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) del pin chiamare il metodo [**CBaseStreamControl:: Flushing**](cbasestreamcontrol-flushing.md) .

La `CBaseStreamControl` classe usa l'orologio di riferimento del grafo del filtro per determinare quali campioni devono essere recapitati dal filtro e quali devono essere rimossi. Nel metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del pin chiamare il metodo [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) con un puntatore all'esempio di supporto in entrata. Se il metodo restituisce il flusso del flusso \_ di valori, fornire l'esempio downstream. In caso contrario, eliminarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




