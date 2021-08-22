---
description: La classe CEnumPins implementa un enumeratore per i pin.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: Classe CEnumPins (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7135a07aedb879503d36011b274bdeab8035924b91bb5d9bc656d6d89dfbe201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567006"
---
# <a name="cenumpins-class"></a>Classe CEnumPins

![Gerarchia di classi cenumpins](images/filter03.png)

La `CEnumPins` classe implementa un enumeratore per i pin.

Questa classe implementa [**l'interfaccia IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) Chiama i metodi [**CBaseFilter**](cbasefilter.md) seguenti:

-   [**CBaseFilter::GetPin:**](cbasefilter-getpin.md)recupera un segnaposto sul filtro, a cui fa riferimento un indice in base zero.
-   [**CBaseFilter::GetPinCount:**](cbasefilter-getpincount.md)recupera il numero totale di pin nel filtro.
-   [**CBaseFilter::GetPinVersion:**](cbasefilter-getpinversion.md)determina se i pin sono stati modificati.

Se il filtro crea o elimina in modo dinamico i pin, incrementa la versione del pin ogni volta che i pin cambiano. Se il numero di versione cambia, l'oggetto enumeratore non viene più sincronizzato con il filtro. Quando l'enumeratore non è sincronizzato, i metodi in `CEnumPins` restituiscono VFW \_ \_ ENUM \_ OUT OF \_ \_ SYNC. Chiamare il [**metodo CEnumPins::Reset**](cenumpins-reset.md) per risincronizzare l'enumeratore.



| Metodi pubblici                             | Descrizione                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [**CEnumPins**](cenumpins-cenumpins.md)   | Metodo del costruttore.                                             |
| [**~CEnumPins**](cenumpins--cenumpins.md) | Metodo del distruttore. Virtuale.                                     |
| Metodi IEnumPins                          | Descrizione                                                     |
| [**Clone**](cenumpins-clone.md)           | Crea una copia dell'enumeratore con lo stesso stato di enumerazione. |
| [**Avanti**](cenumpins-next.md)             | Recupera un numero specificato di pin.                           |
| [**Reset**](cenumpins-reset.md)           | Riporta all'inizio la sequenza di enumerazione.               |
| [**Ignora**](cenumpins-skip.md)             | Ignora un numero specificato di pin.                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




