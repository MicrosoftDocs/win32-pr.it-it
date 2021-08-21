---
description: La classe CBaseMediaFilter implementa l'interfaccia IMediaFilter.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: Classe CBaseMediaFilter (Amfilter.h)
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
ms.openlocfilehash: 16225ca289597bd8145e689912fd458a4f29d8aa4cc5ca68d6c3e0d0e3605ccc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586106"
---
# <a name="cbasemediafilter-class"></a>Classe CBaseMediaFilter

![cbasemediafilter](images/filter05.png)

La `CBaseMediaFilter` classe implementa [**l'interfaccia IMediaFilter.**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) Usare questa classe per i distributori plug-in o altri oggetti che devono supportare **IMediaFilter** senza supportare [**l'interfaccia IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) Non usare questa classe per i filtri. Usare invece la [**classe CBaseFilter**](cbasefilter.md) o una classe di base derivata da **CBaseFilter**.



| Variabili membro protette                                       | Descrizione                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [**m \_ Stato**](cbasemediafilter-m-state.md)                     | Stato corrente dell'oggetto .                                 |
| [**m \_ pClock**](cbasemediafilter-m-pclock.md)                   | Puntatore all'orologio di riferimento dell'oggetto.                     |
| [**m \_ tStart**](cbasemediafilter-m-tstart.md)                   | Ora di riferimento corrispondente all'ora del flusso 0.            |
| [**m \_ clsid**](cbasemediafilter-m-clsid.md)                     | Identificatore di classe (CLSID) dell'oggetto.                      |
| [**m \_ pLock**](cbasemediafilter-m-plock.md)                     | Puntatore a una sezione critica.                               |
| Metodi pubblici                                                   | Descrizione                                                  |
| [**CBaseMediaFilter**](cbasemediafilter-cbasemediafilter.md)    | Metodo del costruttore.                                          |
| [**~ CBaseMediaFilter**](cbasemediafilter--cbasemediafilter.md) | Metodo del distruttore. Virtuale.                                  |
| [**StreamTime**](cbasemediafilter-streamtime.md)                | Recupera l'ora corrente del flusso. Virtuale.                  |
| [**Isactive**](cbasemediafilter-isactive.md)                    | Determina se l'oggetto è attivo (in esecuzione o sospeso). |
| Metodi IPersist                                                 | Descrizione                                                  |
| [**GetClassID**](cbasemediafilter-getclassid.md)                | Recupera l'identificatore di classe.                              |
| Metodi IMediaFilter                                             | Descrizione                                                  |
| [**GetState**](cbasemediafilter-getstate.md)                    | Recupera lo stato dell'oggetto (in esecuzione, arrestato o sospeso).  |
| [**SetSyncSource**](cbasemediafilter-setsyncsource.md)          | Imposta un clock di riferimento per l'oggetto .                       |
| [**GetSyncSource**](cbasemediafilter-getsyncsource.md)          | Recupera l'orologio di riferimento utilizzato dall'oggetto .      |
| [**Fermare**](cbasemediafilter-stop.md)                            | Arresta l'oggetto .                                            |
| [**Sospendi**](cbasemediafilter-pause.md)                          | Sospende l'oggetto .                                           |
| [**Esegui**](cbasemediafilter-run.md)                              | Esegue l'oggetto .                                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




