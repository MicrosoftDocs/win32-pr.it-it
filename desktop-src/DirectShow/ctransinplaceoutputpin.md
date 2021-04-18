---
description: La classe CTransInPlaceOutputPin implementa un pin di output usato dalla classe CTransInPlaceFilter.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Classe CTransInPlaceOutputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326168"
---
# <a name="ctransinplaceoutputpin-class"></a>Classe CTransInPlaceOutputPin

![gerarchia di classi ctransinplaceoutputpin](images/tsip02.png)

La `CTransInPlaceOutputPin` classe implementa un pin di output usato dalla classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .

In genere, non è necessario derivare da questa classe. In tal caso, è necessario eseguire l'override del metodo [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) del filtro per creare istanze della classe derivata.



| Variabili membro protette                                                      | Descrizione                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**\_pTIPFilter m**](ctransinplaceoutputpin-m-ptipfilter.md)                    | Puntatore al filtro che ha creato questo pin.         |
| Metodi pubblici                                                                  | Descrizione                                          |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | Metodo del costruttore.                                  |
| [**CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md)                 | Determina se il pin accetta un tipo di supporto specifico. |
| [**Seallocator**](ctransinplaceoutputpin-setallocator.md)                     | Specifica un allocatore per la connessione.           |
| [**ConnectedIMemInputPin**](ctransinplaceoutputpin-connectedimeminputpin.md)   | Recupera un puntatore al pin di input downstream.     |
| [**PeekAllocator**](ctransinplaceoutputpin-peekallocator.md)                   | Recupera un puntatore all'allocatore del PIN.          |
| Metodi IPin                                                                    | Descrizione                                          |
| [**EnumMediaTypes**](ctransinplaceoutputpin-enummediatypes.md)                 | Enumera i tipi di supporto preferiti del PIN.          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




