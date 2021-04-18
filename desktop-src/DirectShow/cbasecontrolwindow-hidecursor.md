---
description: Il metodo HideCursor nasconde o Visualizza il cursore.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Metodo CBaseControlWindow. HideCursor (Ctlutil. h)
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
ms.openlocfilehash: d0f379c719052de77b54dba47f83b34ae235415f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329266"
---
# <a name="cbasecontrolwindowhidecursor-method"></a>CBaseControlWindow. HideCursor, metodo

Il `HideCursor` metodo nasconde o Visualizza il cursore.

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

Valore che specifica se visualizzare il cursore. Impostare su OATRUE per nascondere il cursore oppure OAFALSE per visualizzare il cursore.

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

 

 




