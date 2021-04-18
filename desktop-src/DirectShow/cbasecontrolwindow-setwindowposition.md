---
description: Il metodo SetWindowPosition imposta la posizione della finestra sul desktop.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Metodo CBaseControlWindow. SetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329866"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a>CBaseControlWindow. SetWindowPosition, metodo

Il `SetWindowPosition` metodo imposta la posizione della finestra sul desktop.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Sinistra* 
</dt> <dd>

Nuova coordinata sinistra.

</dd> <dt>

*Top* 
</dt> <dd>

Nuova coordinata superiore.

</dd> <dt>

*Larghezza* 
</dt> <dd>

Larghezza della finestra.

</dd> <dt>

*Altezza* 
</dt> <dd>

Altezza della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




