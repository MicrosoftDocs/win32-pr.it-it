---
description: Il metodo DoneWithWindow Elimina la finestra.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Metodo CBaseWindow. DoneWithWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325332"
---
# <a name="cbasewindowdonewithwindow-method"></a>CBaseWindow. DoneWithWindow, metodo

Il `DoneWithWindow` metodo elimina la finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Chiamare questo metodo dal metodo distruttore dell'oggetto derivato.

Se questo metodo viene chiamato dallo stesso thread che ha creato la finestra, il metodo esegue le azioni seguenti:

-   Chiama il metodo [**CBaseWindow:: InactivateWindow**](cbasewindow-inactivatewindow.md) , che disattiva la finestra.
-   Chiama il metodo [**CBaseWindow:: UninitialiseWindow**](cbasewindow-uninitialisewindow.md) , che rilascia le risorse usate dalla finestra.
-   Elimina definitivamente la finestra.

Se il thread `DoneWithWindow` che chiama non è il thread che ha creato la finestra, il metodo invia un messaggio "Destroy" privato alla finestra. Quando la finestra riceve questo messaggio, chiama `DoneWithWindow` su se stesso. Se [**CBaseWindow:: m \_ BDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) è **true**, la finestra Invia il messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




