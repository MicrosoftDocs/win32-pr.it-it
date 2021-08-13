---
description: 'Metodo CBaseOutputPin.CheckConnect: il metodo CheckConnect determina se una connessione pin è adatta.'
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Metodo CBaseOutputPin.CheckConnect (Amfilter.h)
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
ms.openlocfilehash: ca35cb98f279674285610fbd06b0399e93a68d59749fe4129475ab8bd970824a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658864"
---
# <a name="cbaseoutputpincheckconnect-method"></a>Metodo CBaseOutputPin.CheckConnect

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

Puntatore all'interfaccia [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti.



| Codice restituito                                                                                               | Descrizione                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Operazione completata.<br/>                                                         |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>             | Il pin di input non supporta [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> |
| <dl> <dt>**DIREZIONE VFW \_ E \_ NON \_ VALIDA**</dt> </dl> | Le indicazioni stradali non sono compatibili.<br/>                               |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) della classe base e quindi esegue una query sul pin di input per [**l'interfaccia IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




