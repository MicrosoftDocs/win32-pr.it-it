---
description: La classe CEnumPins implementa un enumeratore per i pin.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: Classe CEnumPins (Amfilter. h)
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
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329832"
---
# <a name="cenumpins-class"></a>Classe CEnumPins

![gerarchia di classi cenumpins](images/filter03.png)

La `CEnumPins` classe implementa un enumeratore per i pin.

Questa classe implementa l'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) . Chiama i metodi [**CBaseFilter**](cbasefilter.md) seguenti:

-   [**CBaseFilter:: GetPin**](cbasefilter-getpin.md): Recupera un pin sul filtro, a cui fa riferimento un indice in base zero.
-   [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md): Recupera il numero totale di pin sul filtro.
-   [**CBaseFilter:: GetPinVersion**](cbasefilter-getpinversion.md): determina se i pin sono stati modificati.

Se il filtro crea o Elimina in modo dinamico i pin, incrementa la versione del PIN ogni volta che i pin cambiano. Se il numero di versione viene modificato, l'oggetto enumeratore non viene più sincronizzato con il filtro. Una volta che l'enumeratore non è sincronizzato, i metodi in `CEnumPins` restituiscono la \_ \_ sincronizzazione di VFW E enum \_ \_ \_ . Chiamare il metodo [**CEnumPins:: Reset**](cenumpins-reset.md) per risincronizzare l'enumeratore.



| Metodi pubblici                             | Descrizione                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [**CEnumPins**](cenumpins-cenumpins.md)   | Metodo del costruttore.                                             |
| [**~ CEnumPins**](cenumpins--cenumpins.md) | Metodo del distruttore. Virtuale.                                     |
| Metodi IEnumPins                          | Descrizione                                                     |
| [**Clone**](cenumpins-clone.md)           | Crea una copia dell'enumeratore con lo stesso stato di enumerazione. |
| [**Avanti**](cenumpins-next.md)             | Recupera un numero specificato di pin.                           |
| [**Reset**](cenumpins-reset.md)           | Riporta all'inizio la sequenza di enumerazione.               |
| [**Ignora**](cenumpins-skip.md)             | Ignora un numero specificato di pin.                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




