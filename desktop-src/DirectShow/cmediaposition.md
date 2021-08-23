---
description: La classe CMediaPosition gestisce i metodi IDispatch dell'interfaccia duale IMediaPosition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: Classe CMediaPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7305d5eded589e167352ce7ff13194b52965b939daf907e8381b64684a03d1bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634851"
---
# <a name="cmediaposition-class"></a>Classe CMediaPosition

![Gerarchia di classi cmediaposition](images/cutil14.png)

La **classe CMediaPosition** gestisce i **metodi IDispatch** dell'interfaccia duale [**IMediaPosition.**](/windows/desktop/api/Control/nn-control-imediaposition)

Questa classe eredita [**l'interfaccia IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) ma non la implementa. Implementa **IDispatch tramite** la [**classe CBaseDispatch**](cbasedispatch.md) e la DirectShow dei tipi. Non usare questa classe direttamente. Usare invece una delle classi seguenti:

-   Filtri di origine: usare la classe di base [**CSourceSeeking**](csourceseeking.md) per implementare la ricerca.
-   Filtri di trasformazione: usare la [**classe CPosPassThru**](cpospassthru.md) per passare i comandi di ricerca a monte.
-   Renderer: usare la [**classe CRendererPosPassThru**](crendererpospassthru.md) per passare i comandi di ricerca a monte.



| Metodi pubblici                                              | Descrizione                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CMediaPosition**](cmediaposition-cmediaposition.md)     | Metodo del costruttore.                                                                                                 |
| Metodi IDispatch                                           | Descrizione                                                                                                         |
| [**Getidsofnames**](cmediaposition-getidsofnames.md)       | Mappe un set di nomi a un set corrispondente di DISPID.                                                              |
| [**GetTypeInfo**](cmediaposition-gettypeinfo.md)           | Recupera le informazioni sul tipo per l'oggetto, che possono quindi essere usate per ottenere le informazioni sul tipo per un'interfaccia. |
| [**GetTypeInfoCount**](cmediaposition-gettypeinfocount.md) | Recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.                                            |
| [**evocare**](cmediaposition-invoke.md)                     | Fornisce l'accesso alle proprietà e ai metodi esposti dall'oggetto .                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Classi di base](directshow-base-classes.md)
</dt> </dl>

 

 




