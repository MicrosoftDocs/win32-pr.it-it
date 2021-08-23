---
description: Il metodo PossiblyEatMessage consente a una classe derivata di inoltrare messaggi a un'altra finestra.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Metodo CBaseWindow.PossiblyEatMessage (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851f46d14f949a49c9422256f9b2bda1ba314e5789773121387e89c011f7a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016459"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a>Metodo CBaseWindow.PossiblyEatMessage

Il `PossiblyEatMessage` metodo consente a una classe derivata di inoltrare messaggi a un'altra finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Umsg* 
</dt> <dd>

Identificatore del messaggio.

</dd> <dt>

*wParam* 
</dt> <dd>

Primo parametro del messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

Secondo parametro del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il messaggio è stato inoltrato oppure FALSE in **caso** contrario. La classe base restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Prima che [**il metodo CBaseWindow::OnReceiveMessage**](cbasewindow-onreceivemessage.md) gestisca un messaggio, chiama `PossiblyEatMessage` . Se `PossiblyEatMessage` restituisce **TRUE,** **OnReceiveMessage** ignora il messaggio. Una classe derivata può eseguire l'override `PossiblyEatMessage` di in modo da inoltrare alcuni messaggi a una finestra proprietaria. Ad esempio, la [**classe CBaseControlWindow,**](cbasecontrolwindow.md) che deriva da **CBaseWindow,** inoltra i messaggi della tastiera e del mouse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




