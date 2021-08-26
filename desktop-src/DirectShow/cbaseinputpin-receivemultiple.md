---
description: Il metodo ReceiveMultiple riceve una matrice di esempi. Questo metodo implementa il metodo IMemInputPin::ReceiveMultiple.
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Metodo CBaseInputPin.ReceiveMultiple (Amfilter.h)
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
ms.openlocfilehash: 63d71f47978a2eefdcbdacbe1c31bfe69c732c24a0479357b35aa1ddd2b0a9de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079401"
---
# <a name="cbaseinputpinreceivemultiple-method"></a>Metodo CBaseInputPin.ReceiveMultiple

Il `ReceiveMultiple` metodo riceve una matrice di esempi. Questo metodo implementa il [**metodo IMemInputPin::ReceiveMultiple.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)

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

Indirizzo di una matrice di [**puntatori IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) di dimensioni *nSamples*.

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

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                             | Descrizione                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Operazione completata.<br/>                                        |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | Il pin è attualmente in fase di scaricamento; L'esempio è stato rifiutato.<br/> |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>               | Argomento del puntatore **NULL.**<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo di supporto non valido.<br/>                             |
| <dl> <dt>**ERRORE DI RUNTIME DI VFW \_ E \_ \_**</dt> </dl>   | Si è verificato un errore di run-time.<br/>                      |
| <dl> <dt>**VFW \_ E \_ STATO \_ ERRATO**</dt> </dl>     | Il pin è stato arrestato.<br/>                             |



 

## <a name="remarks"></a>Commenti

Questo metodo si comporta come [**il metodo CBaseInputPin::Receive,**](cbaseinputpin-receive.md) ma riceve una matrice di esempi. Nella classe di base il metodo esegue un ciclo nella matrice e chiama **Receive** con ogni esempio. Eseguire l'override di questa funzione se il filtro può elaborare batch di campioni in modo più efficiente rispetto a elaborarli uno alla volta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




