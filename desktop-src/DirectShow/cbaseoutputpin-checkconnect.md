---
description: Il metodo CheckConnect determina se una connessione pin è adatta.
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Metodo CBaseOutputPin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3274e47e9a77d86f350c17aaca04ec0cdb95ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329553"
---
# <a name="cbaseoutputpincheckconnect-method"></a>CBaseOutputPin. CheckConnect, metodo

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

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** .



| Codice restituito                                                                                               | Descrizione                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                      | Esito positivo.<br/>                                                         |
| <dl> <dt>**E \_ NOinterface**</dt> </dl>             | Il pin di input non supporta [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).<br/> |
| <dl> <dt>**\_direzione VFW E \_ non valida \_**</dt> </dl> | Le direzioni del PIN non sono compatibili.<br/>                               |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) della classe di base e quindi esegue una query sul pin di input per la relativa interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




