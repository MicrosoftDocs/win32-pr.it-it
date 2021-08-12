---
description: Il metodo put \_ Height imposta l'altezza della finestra.
ms.assetid: 11026ee5-e83a-4d82-9069-a302d55a2d46
title: CBaseControlWindow.put_Height metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34774d366858e9c9bbe9ce5b02e897453bca21b9bd07d9eb11c60ac8313d33e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660038"
---
# <a name="cbasecontrolwindowput_height-method"></a>Metodo CBaseControlWindow.put \_ Height

Il `put_Height` metodo imposta l'altezza della finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Height(
   long Height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Altezza* 
</dt> <dd>

Nuova altezza della finestra, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

La finestra ha una posizione sul desktop. Espressa in pixel da quattro coordinate (sinistra, superiore, destra e inferiore). Le interfacce automatizzate da OLE in genere esprimono questa posizione a sinistra, all'inizio, alla larghezza e all'altezza; Questa è la convenzione usata in DirectShow. Tutte le coordinate sono espresse in pixel e la modifica di qualsiasi coordinata aggiornerà immediatamente la finestra.

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

 

 




