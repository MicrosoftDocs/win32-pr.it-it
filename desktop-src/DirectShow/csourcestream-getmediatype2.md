---
description: Il metodo GetMediaType recupera un tipo di supporto preferito.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: Metodo CSourceStream.GetMediaType (Source.h) - parametro pMediaType
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
ms.openlocfilehash: 2850d08726337f1ff43ad09319aea8b0af95d107ad9dad9c0f89ce94474c7261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073195"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a>Metodo CSourceStream.GetMediaType (Source.h)

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

Puntatore a [**un oggetto CMediaType**](cmediatype.md) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                            | Descrizione                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione completata.<br/>              |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Indice non compreso nell'intervallo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Indice minore di zero.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>           | Errore imprevisto.<br/>     |



 

## <a name="remarks"></a>Commenti

Esistono due versioni di questo metodo. Una versione esegue l'override [**del metodo CBasePin::GetMediaType**](cbasepin-getmediatype.md) e accetta un valore di indice come parametro. L'altra versione è progettata per recuperare un singolo tipo di supporto, pertanto manca il parametro index.

Il metodo a parametro singolo restituisce E \_ UNEXPECTED. Il metodo a due parametri verifica che il *parametro iPosition* sia zero e quindi chiama la versione a parametro singolo. A seconda del numero di tipi di supporti supportati dal pin, è necessario eseguire l'override di uno di questi metodi:

-   Se il pin supporta esattamente un tipo di supporto, eseguire l'override della versione a parametro singolo. Compilare il tipo di supporto supportato dal segnaposto.
-   Se il pin supporta più di un tipo di supporto, eseguire l'override della versione a due parametri. Eseguire anche l'override [**del metodo CSourceStream::CheckMediaType.**](csourcestream-checkmediatype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




