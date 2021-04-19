---
description: La classe CBaseMediaFilter implementa l'interfaccia IMediaFilter.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: Classe CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326433"
---
# <a name="cbasemediafilter-class"></a>Classe CBaseMediaFilter

![cbasemediafilter](images/filter05.png)

La `CBaseMediaFilter` classe implementa l'interfaccia [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) . Usare questa classe per i distributori di plug-in o altri oggetti che devono supportare **IMediaFilter** senza supportare l'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . Non usare questa classe per i filtri. Usare invece la classe [**CBaseFilter**](cbasefilter.md) o una classe di base derivata da **CBaseFilter**.



| Variabili membro protette                                       | Descrizione                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [**m \_ stato**](cbasemediafilter-m-state.md)                     | Stato corrente dell'oggetto.                                 |
| [**\_pClock m**](cbasemediafilter-m-pclock.md)                   | Puntatore al clock di riferimento dell'oggetto.                     |
| [**\_tStart m**](cbasemediafilter-m-tstart.md)                   | Tempo di riferimento che corrisponde al tempo di flusso 0.            |
| [**\_CLSID m**](cbasemediafilter-m-clsid.md)                     | Identificatore di classe (CLSID) dell'oggetto.                      |
| [**\_pLock m**](cbasemediafilter-m-plock.md)                     | Puntatore a una sezione critica.                               |
| Metodi pubblici                                                   | Descrizione                                                  |
| [**CBaseMediaFilter**](cbasemediafilter-cbasemediafilter.md)    | Metodo del costruttore.                                          |
| [**~ CBaseMediaFilter**](cbasemediafilter--cbasemediafilter.md) | Metodo del distruttore. Virtuale.                                  |
| [**StreamTime**](cbasemediafilter-streamtime.md)                | Recupera l'ora corrente del flusso. Virtuale.                  |
| [**IsActive**](cbasemediafilter-isactive.md)                    | Determina se l'oggetto è attivo (in esecuzione o in pausa). |
| Metodi IPersist                                                 | Descrizione                                                  |
| [**GetClassID**](cbasemediafilter-getclassid.md)                | Recupera l'identificatore di classe.                              |
| Metodi IMediaFilter                                             | Descrizione                                                  |
| [**GetState**](cbasemediafilter-getstate.md)                    | Recupera lo stato dell'oggetto (in esecuzione, arrestato o sospeso).  |
| [**SetSyncSource**](cbasemediafilter-setsyncsource.md)          | Imposta un clock di riferimento per l'oggetto.                       |
| [**GetSyncSource**](cbasemediafilter-getsyncsource.md)          | Recupera l'orologio di riferimento usato dall'oggetto.      |
| [**Interrompere**](cbasemediafilter-stop.md)                            | Arresta l'oggetto.                                            |
| [**Sospendere**](cbasemediafilter-pause.md)                          | Sospende l'oggetto.                                           |
| [**Correre**](cbasemediafilter-run.md)                              | Esegue l'oggetto.                                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




