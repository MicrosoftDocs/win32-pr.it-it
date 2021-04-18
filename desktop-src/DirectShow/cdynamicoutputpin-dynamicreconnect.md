---
description: Il metodo DynamicReconnect esegue una riconnessione dinamica con un nuovo tipo di supporto. La riconnessione può verificarsi durante l'esecuzione del grafico dei filtri.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Metodo CDynamicOutputPin. DynamicReconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324183"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a>CDynamicOutputPin. DynamicReconnect, metodo

Il `DynamicReconnect` metodo esegue una riconnessione dinamica con un nuovo tipo di supporto. La riconnessione può verificarsi durante l'esecuzione del grafico dei filtri.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                            | Descrizione                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                                                                                                                                 |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Esito negativo. Probabilmente il filtro proprietario non ha chiamato il metodo [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) .<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato dallo stesso thread che recapita i dati al pin. Una volta chiamato questo metodo, non è possibile recapitare gli esempi con il vecchio tipo di supporto. Il chiamante deve assicurarsi che non siano presenti esempi obsoleti in sospeso.

Chiamare [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) prima di chiamare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




