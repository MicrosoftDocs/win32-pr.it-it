---
description: Il metodo GetMediaType recupera un tipo di supporto preferito. Questo metodo usa i *parametri iPosition* *e pMediaType.*
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: Metodo CSourceStream.GetMediaType (Source.h) - Parametri iPosition e pMediaType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb3095e366a03d94616d45eda441fec78d2ccbf7d58f8e74890a42902bae6fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073255"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a>Metodo CSourceStream.GetMediaType (Source.h) - Parametri iPosition e pMediaType

Il **metodo GetMediaType** recupera un tipo di supporto preferito.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iPosition* 
</dt> <dd>

Valore di indice in base zero.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione completata.<br/>              |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Indice non compreso nell'intervallo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Indice minore di zero.<br/> |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl>           | Errore imprevisto.<br/>     |



 

## <a name="remarks"></a>Commenti

Esistono due versioni di questo metodo. Una versione esegue l'override del metodo [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) e accetta un valore di indice come parametro. L'altra versione è progettata per recuperare un singolo tipo di supporto, pertanto manca il parametro index.

Il metodo a parametro singolo restituisce E \_ UNEXPECTED. Il metodo a due parametri verifica che il *parametro iPosition* sia zero e quindi chiama la versione a parametro singolo. A seconda del numero di tipi di supporti supportati dal pin, è necessario eseguire l'override di uno di questi metodi:

-   Se il pin supporta esattamente un tipo di supporto, eseguire l'override della versione a parametro singolo. Compilare il tipo di supporto supportato dal segnaposto.
-   Se il pin supporta più di un tipo di supporto, eseguire l'override della versione a due parametri. Eseguire anche [**l'override del metodo CSourceStream::CheckMediaType.**](csourcestream-checkmediatype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | Source.h (include Flussi.h)                                                                                    |
| Libreria | Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




