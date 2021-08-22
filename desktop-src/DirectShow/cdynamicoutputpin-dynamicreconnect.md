---
description: Il metodo DynamicReconnect esegue una riconnessione dinamica con un nuovo tipo di supporto. La riconnessione può verificarsi durante l'esecuzione del grafico dei filtri.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Metodo CDynamicOutputPin.DynamicReconnect (Amfilter.h)
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
ms.openlocfilehash: 6abd453b328a22765a9649e69bbe0f5e3e4d4bc8e45148a0777fa23901447ab3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688841"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a>Metodo CDynamicOutputPin.DynamicReconnect

Il `DynamicReconnect` metodo esegue una riconnessione dinamica con un nuovo tipo di supporto. La riconnessione può verificarsi durante l'esecuzione del grafico dei filtri.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntatore a una [**struttura AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                            | Descrizione                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                                                                                                                                 |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Esito negativo. È possibile che il filtro proprietario non abbia chiamato il [**metodo CDynamicOutputPin::SetConfigInfo.**](cdynamicoutputpin-setconfiginfo.md)<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato dallo stesso thread che recapita i dati al pin. Una volta chiamato questo metodo, non è possibile recapitare esempi con il tipo di supporto precedente. Il chiamante deve assicurarsi che non siano in sospeso esempi vecchi.

Chiamare [**CDynamicOutputPin::StartUsingOutputPin prima**](cdynamicoutputpin-startusingoutputpin.md) di chiamare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




