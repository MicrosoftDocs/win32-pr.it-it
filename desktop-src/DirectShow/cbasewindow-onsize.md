---
description: Il metodo OnSize gestisce i messaggi WM \_ SIZE.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Metodo CBaseWindow.OnSize (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf6c7793af3cb7866ddaaaae8823acd91ed10ac71d939af8bc9e71eff768d75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657656"
---
# <a name="cbasewindowonsize-method"></a>Metodo CBaseWindow.OnSize

Il `OnSize` metodo gestisce i messaggi WM \_ SIZE.

## <a name="syntax"></a>Sintassi


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Larghezza* 
</dt> <dd>

Larghezza dell'area client, in pixel.

</dd> <dt>

*Altezza* 
</dt> <dd>

Altezza dell'area client, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE.**

## <a name="remarks"></a>Commenti

Questo metodo archivia la nuova larghezza e altezza. Per recuperare questi valori, chiamare i metodi [**CBaseWindow::GetWindowHeight**](cbasewindow-getwindowheight.md) e [**CBaseWindow::GetWindowWidth.**](cbasewindow-getwindowwidth.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




