---
description: Il metodo put \_ Width imposta la larghezza della finestra.
ms.assetid: eb5ad1c2-ba39-4c06-84d2-6708dc8796d8
title: CBaseControlWindow.put_Width metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f32175fe2b86f3b05105f5627cf1e02b2509e25ee12cc415cd88ea2baba5536
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635711"
---
# <a name="cbasecontrolwindowput_width-method"></a>Metodo CBaseControlWindow.put \_ Width

Il `put_Width` metodo imposta la larghezza della finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Width(
   long Width
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Larghezza* 
</dt> <dd>

Nuova larghezza della finestra, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

La finestra ha una posizione sul desktop. Questo valore è espresso in pixel da quattro coordinate (sinistra, superiore, destra e inferiore). Le interfacce automatizzate da OLE in genere esprimono questa posizione a sinistra, in alto, in larghezza e in altezza; questa è la convenzione usata in DirectShow. Tutte le coordinate sono espresse in pixel e la modifica di qualsiasi coordinata aggiornerà immediatamente la finestra.

Se si impostano le coordinate sinistra o superiore, la finestra viene spostata rispettivamente verso sinistra o verso l'alto. queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra. Analogamente, l'impostazione della larghezza e dell'altezza non influisce sulle coordinate sinistra e superiore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




