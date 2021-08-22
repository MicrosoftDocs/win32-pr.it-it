---
description: Il metodo DoneWithWindow elimina la finestra.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Metodo CBaseWindow.DoneWithWindow (Winutil.h)
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
ms.openlocfilehash: c6871a42e1a08693a7daf691195b86cd5a41dd208295dc625a33e41083b53adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016669"
---
# <a name="cbasewindowdonewithwindow-method"></a>Metodo CBaseWindow.DoneWithWindow

Il `DoneWithWindow` metodo elimina la finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Chiamare questo metodo dal metodo del distruttore dell'oggetto derivato.

Se questo metodo viene chiamato dallo stesso thread che ha creato la finestra, il metodo esegue le azioni seguenti:

-   Chiama il [**metodo CBaseWindow::InactivateWindow,**](cbasewindow-inactivatewindow.md) che disattiva la finestra.
-   Chiama il [**metodo CBaseWindow::UninitialiseWindow,**](cbasewindow-uninitialisewindow.md) che rilascia le risorse usate dalla finestra.
-   Elimina la finestra.

Se il thread che chiama non è il thread che ha creato la finestra, il metodo invia un messaggio `DoneWithWindow` privato "destroy" alla finestra. Quando la finestra riceve questo messaggio, chiama `DoneWithWindow` su se stessa. Se [**CBaseWindow::m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) è **TRUE,** la finestra invia il messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




