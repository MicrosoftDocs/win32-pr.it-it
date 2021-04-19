---
description: Il metodo GetMediaType recupera un tipo di supporto preferito.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: Metodo CSourceStream. GetMediaType (source. h)-parametro pMediaType
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
ms.openlocfilehash: 8306da8451d4af7da8ce4f4c7d4d3f6fd367e1ec
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389184"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a>Metodo CSourceStream. GetMediaType (source. h)

Il `GetMediaType` metodo recupera un tipo di supporto preferito.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

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
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




