---
description: La classe CTransInPlaceOutputPin implementa un pin di output usato dalla classe CTransInPlaceFilter.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Classe CTransInPlaceOutputPin (Transip.h)
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
ms.openlocfilehash: 2462843f9ad42793a9e0666dd96aaf7387a1f5f0f1749f97cc4e2ca4d3ed051a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076156"
---
# <a name="ctransinplaceoutputpin-class"></a>Classe CTransInPlaceOutputPin

![Gerarchia di classi ctransinplaceoutputpin](images/tsip02.png)

La `CTransInPlaceOutputPin` classe implementa un pin di output usato dalla classe [**CTransInPlaceFilter.**](ctransinplacefilter.md)

In genere, non è necessario derivare da questa classe. In caso contrario, è necessario eseguire l'override del metodo [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) del filtro per creare istanze della classe derivata.



| Variabili membro protette                                                      | Descrizione                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**m \_ pTIPFilter**](ctransinplaceoutputpin-m-ptipfilter.md)                    | Puntatore al filtro che ha creato questo segnaposto.         |
| Metodi pubblici                                                                  | Descrizione                                          |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | Metodo del costruttore.                                  |
| [**CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md)                 | Determina se il pin accetta un tipo di supporto specifico. |
| [**SetAllocator**](ctransinplaceoutputpin-setallocator.md)                     | Specifica un allocatore per la connessione.           |
| [**ConnectedIMemInputPin**](ctransinplaceoutputpin-connectedimeminputpin.md)   | Recupera un puntatore al pin di input downstream.     |
| [**PeekAllocator**](ctransinplaceoutputpin-peekallocator.md)                   | Recupera un puntatore all'allocatore del pin.          |
| Metodi IPin                                                                    | Descrizione                                          |
| [**EnumMediaTypes**](ctransinplaceoutputpin-enummediatypes.md)                 | Enumera i tipi di supporti preferiti del segnaposto.          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




