---
description: Il metodo CheckConnect determina se una connessione pin è adatta.
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Metodo CTransformInputPin. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e10c174a4e295576cfa9ce902faeac889f5a6a9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328814"
---
# <a name="ctransforminputpincheckconnect-method"></a>CTransformInputPin. CheckConnect, metodo

Il `CheckConnect` metodo determina se una connessione pin è adatta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                               | Descrizione                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                      | Operazione riuscita<br/>             |
| <dl> <dt>**\_direzione VFW E \_ non valida \_**</dt> </dl> | Direzione del pin errata<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) . Chiama il metodo [**CTransformFilter:: CheckConnect**](ctransformfilter-checkconnect.md) del filtro, che restituisce \_ OK nella classe di base. La classe derivata può eseguire l'override del metodo **CTransformFilter:: CheckConnect** per eseguire ulteriori controlli.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




