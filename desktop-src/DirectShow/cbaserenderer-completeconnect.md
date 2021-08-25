---
description: Il metodo CompleteConnect completa la connessione del pin di input a un altro pin.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Metodo CBaseRenderer.CompleteConnect (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 833e19a6e7b100aac5322a54455c04c263569e33b3422d5957e5eeee15bbd283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157842"
---
# <a name="cbaserenderercompleteconnect-method"></a>Metodo CBaseRenderer.CompleteConnect

Il `CompleteConnect` metodo completa la connessione del pin di input a un altro pin.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore all'interfaccia [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il pin di input del filtro chiama questo metodo dall'interno del proprio metodo, che viene chiamato `CompleteConnect` per completare una connessione pin. Per altre informazioni, vedere [**CBasePin::CompleteConnect.**](cbasepin-completeconnect.md) Il filtro chiama il [**metodo CBaseRenderer::SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) per abilitare [**gli eventi EC \_ REPAINT.**](ec-repaint.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




