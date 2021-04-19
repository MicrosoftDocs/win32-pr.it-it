---
description: Il \_ metodo Get Top recupera la coordinata della finestra superiore.
ms.assetid: 1e7910bd-e38e-4586-9dd6-701f69c0f6e7
title: Metodo CBaseControlWindow.get_Top (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9861d930cdb2d93e5e0b73ffad625885c082cb6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332352"
---
# <a name="cbasecontrolwindowget_top-method"></a>Metodo CBaseControlWindow. Get \_ Top

Il `get_Top` metodo recupera la coordinata della finestra superiore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Top(
   long *pTop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTop* 
</dt> <dd>

Puntatore alla coordinata superiore, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

La finestra è posizionata sul desktop. Questo è espresso in pixel da quattro coordinate, a sinistra, in alto, a destra e in basso. Le interfacce automatizzate da OLE generalmente esprimono questa posizione attraverso Left, top, Width e Height. si tratta della convenzione usata in DirectShow. Tutte le coordinate sono espresse in pixel e la modifica di tutte le coordinate aggiornerà immediatamente la finestra.

L'impostazione delle coordinate di sinistra o superiore sposta la finestra verso sinistra o verso l'alto rispettivamente; Queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra. Analogamente, l'impostazione della larghezza e dell'altezza non influisce sulle coordinate di sinistra e di primo livello.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




