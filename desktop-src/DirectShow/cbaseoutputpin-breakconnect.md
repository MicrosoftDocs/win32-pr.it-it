---
description: 'Metodo CBaseOutputPin.BreakConnect: il metodo BreakConnect rilascia il pin da una connessione.'
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Metodo CBaseOutputPin.BreakConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae03edb843a2b9c6f1cbc98a46c2464de0e76e2eecf5d77bc309efa2dd60fd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793221"
---
# <a name="cbaseoutputpinbreakconnect-method"></a>Metodo CBaseOutputPin.BreakConnect

Il `BreakConnect` metodo rilascia il pin da una connessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBasePin::BreakConnect.**](cbasepin-breakconnect.md) Decommita l'allocatore e rilascia [**le interfacce IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) e [**IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo di override. In caso contrario, potrebbero verificarsi perdite di memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




