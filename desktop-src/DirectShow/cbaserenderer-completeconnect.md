---
description: Il metodo CompleteConnect completa la connessione del PIN di input a un altro pin.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Metodo CBaseRenderer. CompleteConnect (Renbase. h)
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
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329393"
---
# <a name="cbaserenderercompleteconnect-method"></a>CBaseRenderer. CompleteConnect, metodo

Il `CompleteConnect` metodo completa la connessione del PIN di input a un altro pin.

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

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Il pin di input del filtro chiama questo metodo dall'interno del proprio `CompleteConnect` metodo, che viene chiamato per completare una connessione del PIN. Per ulteriori informazioni, vedere [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md). Il filtro chiama il metodo [**CBaseRenderer:: SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) per abilitare gli eventi di [**\_ ridisegno EC**](ec-repaint.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




