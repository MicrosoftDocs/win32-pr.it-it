---
description: 'Metodo CTransformOutputPin.CheckConnect: il metodo CheckConnect determina se una connessione pin è adatta.'
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Metodo CTransformOutputPin.CheckConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b85c2197cf65465441387ecc661af71e0ddfa7ca912c3296ddee543d11c4784
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086991"
---
# <a name="ctransformoutputpincheckconnect-method"></a>Metodo CTransformOutputPin.CheckConnect

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

Puntatore all'interfaccia [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                  | Descrizione                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata.<br/>                                 |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl> | Il pin di input del filtro non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseOutputPin::CheckConnect.**](cbaseoutputpin-checkconnect.md) Chiama il metodo [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) del filtro, che restituisce S \_ OK nella classe di base. La classe derivata può eseguire l'override del metodo **CTransformFilter::CheckConnect** per eseguire controlli aggiuntivi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




