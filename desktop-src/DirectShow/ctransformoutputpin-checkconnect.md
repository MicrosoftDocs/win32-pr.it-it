---
description: Il metodo CheckConnect determina se una connessione pin è adatta.
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Metodo CTransformOutputPin. CheckConnect (Transfrm. h)
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
ms.openlocfilehash: b9a20eb8d3e20679cb8805d3a1cd8e167ef0bfd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331455"
---
# <a name="ctransformoutputpincheckconnect-method"></a>CTransformOutputPin. CheckConnect, metodo

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

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                  | Descrizione                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>                                 |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Il pin di input del filtro non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBaseOutputPin:: CheckConnect**](cbaseoutputpin-checkconnect.md) . Chiama il metodo [**CTransformFilter:: CheckConnect**](ctransformfilter-checkconnect.md) del filtro, che restituisce \_ OK nella classe di base. La classe derivata può eseguire l'override del metodo **CTransformFilter:: CheckConnect** per eseguire ulteriori controlli.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




