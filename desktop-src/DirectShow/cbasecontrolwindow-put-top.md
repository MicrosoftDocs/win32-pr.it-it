---
description: Il metodo put \_ Top imposta la coordinata della finestra superiore.
ms.assetid: cd39807f-363d-4b5b-8279-9dfb992dca10
title: CBaseControlWindow.put_Top metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3332bcf90ac5e2ee776fe7110c958e50b838bcbdbc6bb4abb23850ced12cc28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635831"
---
# <a name="cbasecontrolwindowput_top-method"></a>Metodo CBaseControlWindow.put \_ Top

Il `put_Top` metodo imposta la coordinata della finestra superiore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Top(
   long Top
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Top* 
</dt> <dd>

Nuova coordinata superiore, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

La finestra ha una posizione sul desktop. Espressa in pixel da quattro coordinate (sinistra, superiore, destra e inferiore). Le interfacce automatizzate da OLE in genere esprimono questa posizione a sinistra, all'inizio, alla larghezza e all'altezza; questa è la convenzione usata in DirectShow. Tutte le coordinate sono espresse in pixel e la modifica di qualsiasi coordinata aggiornerà immediatamente la finestra.

Se si impostano le coordinate sinistra o superiore, la finestra viene spostata rispettivamente verso sinistra o verso l'alto. Queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra. Analogamente, l'impostazione di larghezza e altezza non influisce sulle coordinate sinistra e superiore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




