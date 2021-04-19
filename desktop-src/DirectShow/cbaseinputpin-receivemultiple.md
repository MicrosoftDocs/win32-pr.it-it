---
description: 'Il metodo ReceiveMultiple riceve una matrice di esempi. Questo metodo implementa il metodo IMemInputPin:: ReceiveMultiple.'
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Metodo CBaseInputPin. ReceiveMultiple (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333213"
---
# <a name="cbaseinputpinreceivemultiple-method"></a>CBaseInputPin. ReceiveMultiple, metodo

Il `ReceiveMultiple` metodo riceve una matrice di campioni. Questo metodo implementa il metodo [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSamples* 
</dt> <dd>

Indirizzo di una matrice di puntatori [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) , di dimensioni *nSamples*.

</dd> <dt>

*nSamples* 
</dt> <dd>

Numero di campioni da elaborare.

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

Puntatore a una variabile che riceve il numero di campioni elaborati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                             | Descrizione                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Esito positivo.<br/>                                        |
| <dl> <dt>**S \_ false**</dt> </dl>                 | Il PIN sta attualmente scaricando; esempio rifiutato.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>               | Argomento puntatore **null** .<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo di supporto non valido.<br/>                             |
| <dl> <dt>**errore di runtime di VFW \_ E \_ \_**</dt> </dl>   | Si è verificato un errore in fase di esecuzione.<br/>                      |
| <dl> <dt>**\_ \_ stato non corretto di VFW E \_**</dt> </dl>     | Il PIN è stato arrestato.<br/>                             |



 

## <a name="remarks"></a>Commenti

Questo metodo si comporta come il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) , ma riceve una matrice di esempi. Nella classe di base il metodo scorre la matrice e chiama **Receive** con ogni campione. Eseguire l'override di questa funzione se il filtro è in grado di elaborare batch di campioni in modo più efficiente rispetto all'elaborazione uno alla volta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




