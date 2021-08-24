---
description: 'Metodo CTransformInputPin.CheckConnect: il metodo CheckConnect determina se una connessione pin è adatta.'
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Metodo CTransformInputPin.CheckConnect (Transfrm.h)
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
ms.openlocfilehash: 9a48bd2d3231979a30f8f7ff0d8144929115c51b9ca3f464f85d6d0163954ad7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823721"
---
# <a name="ctransforminputpincheckconnect-method"></a>Metodo CTransformInputPin.CheckConnect

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

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                               | Descrizione                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Operazione riuscita<br/>             |
| <dl> <dt>**DIREZIONE VFW \_ E \_ NON \_ VALIDA**</dt> </dl> | Direzione del segnaposto errata<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBasePin::CheckConnect.**](cbasepin-checkconnect.md) Chiama il metodo [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) del filtro, che restituisce S \_ OK nella classe di base. La classe derivata può eseguire l'override del metodo **CTransformFilter::CheckConnect** per eseguire controlli aggiuntivi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




