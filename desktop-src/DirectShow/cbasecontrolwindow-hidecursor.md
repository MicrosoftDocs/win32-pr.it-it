---
description: Il metodo HideCursor nasconde o visualizza il cursore.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Metodo CBaseControlWindow.HideCursor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6421a650471d0954031433db3814e8453cbc82586c7f37608ae947e7301c6969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158382"
---
# <a name="cbasecontrolwindowhidecursor-method"></a>Metodo CBaseControlWindow.HideCursor

Il `HideCursor` metodo nasconde o visualizza il cursore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HideCursor* 
</dt> <dd>

Valore che specifica se visualizzare il cursore. Impostare su OATRUE per nascondere il cursore oppure su OAFALSE per visualizzare il cursore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




