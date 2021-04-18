---
description: Il metodo GetMediaType recupera un tipo di supporto preferito. Questo metodo usa i parametri *iPosition* e *pMediaType* .
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: Metodo CSourceStream. GetMediaType (source. h)-parametri iPosition e pMediaType
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
ms.openlocfilehash: 9d8936f08b952af069812859736a6a13ea9c0e4e
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334365"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a>Metodo CSourceStream. GetMediaType (source. h)-parametri iPosition e pMediaType

Il metodo **GetMediaType** recupera un tipo di supporto preferito.

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

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Esito positivo.<br/>              |
| <dl> <dt>**\_non ci \_ sono \_ altri \_ elementi di VFW**</dt> </dl> | Indice non compreso nell'intervallo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Indice minore di zero.<br/> |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>           | Errore imprevisto.<br/>     |



 

## <a name="remarks"></a>Commenti

Sono disponibili due versioni di questo metodo. Una versione esegue l'override del metodo [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) e accetta un valore di indice come parametro. L'altra versione è progettata per recuperare un solo tipo di supporto, pertanto non dispone del parametro index.

Il metodo a parametro singolo restituisce E \_ imprevisto. Il metodo a due parametri verifica che il parametro *iPosition* sia zero, quindi chiama la versione a parametro singolo. A seconda del numero di tipi di supporto supportati dal pin, è necessario eseguire l'override di uno di questi metodi:

-   Se il pin supporta esattamente un tipo di supporto, eseguire l'override della versione a parametro singolo. Compilare il tipo di supporto supportato dal pin.
-   Se il pin supporta più di un tipo di supporto, eseguire l'override della versione a due parametri. Eseguire anche l'override del metodo [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | Source. h (Includi Streams. h)                                                                                    |
| Libreria | Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




