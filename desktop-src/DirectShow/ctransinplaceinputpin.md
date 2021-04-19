---
description: La classe CTransInPlaceInputPin implementa un pin di input usato dalla classe CTransInPlaceFilter.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Classe CTransInPlaceInputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326185"
---
# <a name="ctransinplaceinputpin-class"></a>Classe CTransInPlaceInputPin

![gerarchia di classi ctransinplaceinputpin](images/tsip01.png)

La `CTransInPlaceInputPin` classe implementa un pin di input usato dalla classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .

In genere, non è necessario derivare da questa classe. In tal caso, è necessario eseguire l'override del metodo [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) del filtro per creare istanze della classe derivata.



| Variabili membro protette                                                          | Descrizione                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**\_bReadOnly m**](ctransinplaceinputpin-m-breadonly.md)                           | Flag che specifica se il flusso di input è di sola lettura. |
| [**\_pTIPFilter m**](ctransinplaceinputpin-m-ptipfilter.md)                         | Puntatore al filtro che ha creato questo pin.               |
| Metodi pubblici                                                                      | Descrizione                                                |
| [**CTransInPlaceInputPin**](ctransinplaceinputpin-ctransinplaceinputpin.md)        | Metodo del costruttore.                                        |
| [**CheckMediaType**](ctransinplaceinputpin-checkmediatype.md)                      | Determina se il pin accetta un tipo di supporto specifico.       |
| [**PeekAllocator**](ctransinplaceinputpin-peekallocator.md)                        | Recupera un puntatore all'allocatore del PIN.                |
| [**ReadOnly**](ctransinplaceinputpin-readonly.md)                                  | Indica se il flusso di input è di sola lettura.           |
| Metodi IPin                                                                        | Descrizione                                                |
| [**EnumMediaTypes**](ctransinplaceinputpin-enummediatypes.md)                      | Enumera i tipi di supporto preferiti del PIN.                |
| Metodi IMemInputPin                                                                | Descrizione                                                |
| [**Getallocator**](ctransinplaceinputpin-getallocator.md)                          | Recupera l'allocatore di memoria proposto da questo pin.       |
| [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md)                    | Specifica un allocatore per la connessione.                 |
| [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) | Recupera le proprietà dell'allocatore richieste dal pin.   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




