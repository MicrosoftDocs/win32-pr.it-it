---
description: La classe CTransInPlaceInputPin implementa un pin di input usato dalla classe CTransInPlaceFilter.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Classe CTransInPlaceInputPin (Transip.h)
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
ms.openlocfilehash: 04d30b18d115e7ef03e88deb47355bafc795532a91afa14cf2f4392e658954f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076197"
---
# <a name="ctransinplaceinputpin-class"></a>Classe CTransInPlaceInputPin

![Gerarchia di classi ctransinplaceinputpin](images/tsip01.png)

La `CTransInPlaceInputPin` classe implementa un pin di input usato dalla classe [**CTransInPlaceFilter.**](ctransinplacefilter.md)

In genere, non è necessario derivare da questa classe. In caso contrario, è necessario eseguire l'override del metodo [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) del filtro per creare istanze della classe derivata.



| Variabili membro protette                                                          | Descrizione                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**m \_ bReadOnly**](ctransinplaceinputpin-m-breadonly.md)                           | Flag che specifica se il flusso di input è di sola lettura. |
| [**m \_ pTIPFilter**](ctransinplaceinputpin-m-ptipfilter.md)                         | Puntatore al filtro che ha creato questo segnaposto.               |
| Metodi pubblici                                                                      | Descrizione                                                |
| [**CTransInPlaceInputPin**](ctransinplaceinputpin-ctransinplaceinputpin.md)        | Metodo del costruttore.                                        |
| [**CheckMediaType**](ctransinplaceinputpin-checkmediatype.md)                      | Determina se il pin accetta un tipo di supporto specifico.       |
| [**PeekAllocator**](ctransinplaceinputpin-peekallocator.md)                        | Recupera un puntatore all'allocatore del pin.                |
| [**ReadOnly**](ctransinplaceinputpin-readonly.md)                                  | Indica se il flusso di input è di sola lettura.           |
| Metodi IPin                                                                        | Descrizione                                                |
| [**EnumMediaTypes**](ctransinplaceinputpin-enummediatypes.md)                      | Enumera i tipi di supporti preferiti del segnaposto.                |
| Metodi IMemInputPin                                                                | Descrizione                                                |
| [**GetAllocator**](ctransinplaceinputpin-getallocator.md)                          | Recupera l'allocatore di memoria proposto da questo pin.       |
| [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md)                    | Specifica un allocatore per la connessione.                 |
| [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) | Recupera le proprietà dell'allocatore richieste dal pin.   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




