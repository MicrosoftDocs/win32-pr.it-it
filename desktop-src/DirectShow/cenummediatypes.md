---
description: La classe CEnumMediaTypes implementa un enumeratore per i tipi di supporto preferiti.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: Classe CEnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329844"
---
# <a name="cenummediatypes-class"></a>Classe CEnumMediaTypes

![gerarchia di classi cenummediatypes](images/filter04.png)

La `CEnumMediaTypes` classe implementa un enumeratore per i tipi di supporto preferiti.

Questa classe implementa l'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) . Chiama i metodi [**CBasePin**](cbasepin.md) seguenti:

-   [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md): Recupera un tipo di supporto, a cui fa riferimento un indice in base zero.
-   [**CBasePin:: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): determina se il set di tipi preferiti è stato modificato.

Ogni volta che un pin modifica l'elenco dei tipi di supporto preferiti, il pin incrementa il numero di versione del tipo di supporto. Quando ciò si verifica, l'oggetto enumeratore non è più sincronizzato con il PIN e i metodi della classe restituiscono l'enumerazione VFW e non è \_ \_ \_ \_ \_ sincronizzata. Chiamare il metodo [**CEnumMediaTypes:: Reset**](cenummediatypes-reset.md) per risincronizzare l'enumeratore.



| Metodi pubblici                                               | Descrizione                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [**CEnumMediaTypes**](cenummediatypes-cenummediatypes.md)   | Metodo del costruttore.                                             |
| [**~ CEnumMediaTypes**](cenummediatypes--cenummediatypes.md) | Metodo del distruttore. Virtuale.                                     |
| Metodi IEnumMediaTypes                                      | Descrizione                                                     |
| [**Clone**](cenummediatypes-clone.md)                       | Crea una copia dell'enumeratore con lo stesso stato di enumerazione. |
| [**Avanti**](cenummediatypes-next.md)                         | Recupera un numero specificato di tipi di supporti.                    |
| [**Reset**](cenummediatypes-reset.md)                       | Riporta all'inizio la sequenza di enumerazione.               |
| [**Ignora**](cenummediatypes-skip.md)                         | Ignora un numero specificato di tipi di supporti.                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




