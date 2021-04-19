---
description: La classe CMediaPosition gestisce i metodi IDispatch dell'interfaccia duale IMediaPosition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: Classe CMediaPosition (Ctlutil. h)
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
ms.openlocfilehash: 60d06a08badf3302ef4ddb352d840842a2605600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326409"
---
# <a name="cmediaposition-class"></a>Classe CMediaPosition

![gerarchia di classi cmediaposition](images/cutil14.png)

La classe **CMediaPosition** gestisce i metodi **IDispatch** dell'interfaccia duale [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .

Questa classe eredita l'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) , ma non la implementa. Implementa **IDispatch** tramite la classe [**CBaseDispatch**](cbasedispatch.md) e la libreria dei tipi DirectShow. Non usare direttamente questa classe. Usare invece una delle classi seguenti:

-   Filtri di origine: usare la classe di base [**CSourceSeeking**](csourceseeking.md) per implementare la ricerca.
-   Filtri di trasformazione: usare la classe [**CPosPassThru**](cpospassthru.md) per passare i comandi di ricerca upstream.
-   Renderer: usare la classe [**CRendererPosPassThru**](crendererpospassthru.md) per passare i comandi di ricerca upstream.



| Metodi pubblici                                              | Descrizione                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CMediaPosition**](cmediaposition-cmediaposition.md)     | Metodo del costruttore.                                                                                                 |
| IDispatch (metodi)                                           | Descrizione                                                                                                         |
| [**GetIDsOfNames**](cmediaposition-getidsofnames.md)       | Esegue il mapping di un set di nomi a un set di DISPID corrispondente.                                                              |
| [**GetTypeInfo**](cmediaposition-gettypeinfo.md)           | Recupera le informazioni sul tipo per l'oggetto, che può quindi essere utilizzato per ottenere le informazioni sul tipo per un'interfaccia. |
| [**GetTypeInfoCount**](cmediaposition-gettypeinfocount.md) | Recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.                                            |
| [**Richiamare**](cmediaposition-invoke.md)                     | Fornisce l'accesso alle proprietà e ai metodi esposti dall'oggetto.                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi base di DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




