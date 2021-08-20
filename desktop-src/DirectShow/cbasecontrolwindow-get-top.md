---
description: Il metodo get \_ Top recupera la coordinata della finestra superiore.
ms.assetid: 1e7910bd-e38e-4586-9dd6-701f69c0f6e7
title: CBaseControlWindow.get_Top metodo (Ctlutil.h)
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
ms.openlocfilehash: f7ba60f3365ba2f1a8ea00579e8c2eb51c9d6aa32843e7603d0d26c2747c97c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017389"
---
# <a name="cbasecontrolwindowget_top-method"></a>Metodo CBaseControlWindow.get \_ Top

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

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

La finestra ha una posizione sul desktop. Espressa in pixel da quattro coordinate (sinistra, superiore, destra e inferiore). Le interfacce automatizzate da OLE in genere esprimono questa posizione a sinistra, all'inizio, alla larghezza e all'altezza; questa è la convenzione usata in DirectShow. Tutte le coordinate sono espresse in pixel e la modifica di qualsiasi coordinata aggiornerà immediatamente la finestra.

Se si impostano le coordinate sinistra o superiore, la finestra viene spostata rispettivamente verso sinistra o verso l'alto. Queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra. Analogamente, l'impostazione della larghezza e dell'altezza non influisce sulle coordinate sinistra e superiore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




