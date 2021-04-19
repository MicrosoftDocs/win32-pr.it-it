---
description: Il metodo PossiblyEatMessage consente a una classe derivata di inviare messaggi a un'altra finestra.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Metodo CBaseWindow. PossiblyEatMessage (Winutil. h)
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
ms.openlocfilehash: f218b62ac5464da27b8596992c34ce7ae5efde46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325759"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a>CBaseWindow. PossiblyEatMessage, metodo

Il `PossiblyEatMessage` metodo consente a una classe derivata di inviare messaggi a un'altra finestra.

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

*uMsg* 
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

Restituisce **true** se il messaggio è stato inviato o **false** in caso contrario. La classe base restituisce **false**.

## <a name="remarks"></a>Commenti

Prima che il metodo [**CBaseWindow:: OnReceiveMessage**](cbasewindow-onreceivemessage.md) gestisca un messaggio, chiama `PossiblyEatMessage` . Se `PossiblyEatMessage` restituisce **true**, **OnReceiveMessage** ignora il messaggio. Una classe derivata può eseguire l'override `PossiblyEatMessage` di in modo che inoltri alcuni messaggi a una finestra proprietaria. Ad esempio, la classe [**CBaseControlWindow**](cbasecontrolwindow.md) , che deriva da **CBaseWindow**, trasmette i messaggi della tastiera e del mouse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




