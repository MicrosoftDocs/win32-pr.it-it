---
description: Il metodo get \_ Width recupera la larghezza della finestra corrente.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: CBaseControlWindow.get_Width metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3dff6e2a0929963f06c14aa8899b2a1d6a268db8f87b5067d2ed65f90964c803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768241"
---
# <a name="cbasecontrolwindowget_width-method"></a>Metodo CBaseControlWindow.get \_ Width

Il `get_Width` metodo recupera la larghezza della finestra corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWidth* 
</dt> <dd>

Puntatore alla larghezza della finestra, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

La finestra ha una posizione sul desktop. Questo valore è espresso in pixel da quattro coordinate (sinistra, superiore, destra e inferiore). Le interfacce automatizzate da OLE in genere esprimono questa posizione a sinistra, in alto, in larghezza e in altezza; questa è la convenzione usata in DirectShow. Tutte le coordinate sono espresse in pixel e la modifica di qualsiasi coordinata aggiornerà immediatamente la finestra.

Se si impostano le coordinate sinistra o superiore, la finestra viene spostata verso sinistra o verso l'alto, rispettivamente. queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra. Analogamente, l'impostazione della larghezza e dell'altezza non influisce sulle coordinate sinistra e superiore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




