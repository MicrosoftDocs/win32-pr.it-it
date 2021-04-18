---
description: Il metodo CompleteConnect notifica alla finestra che il pin di input del renderer è stato connesso.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Metodo CBaseWindow. CompleteConnect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325342"
---
# <a name="cbasewindowcompleteconnect-method"></a>CBaseWindow. CompleteConnect, metodo

Il `CompleteConnect` metodo notifica alla finestra che il pin di input del renderer è stato connesso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo reimposta il flag di attivazione della finestra ([**CBaseWindow:: m \_ bActivated**](cbasewindow-m-bactivated.md)) su **false**. Quando un renderer video completa una connessione pin, può chiamare il metodo [**CBaseWindow:: Activatewindow**](cbasewindow-activatewindow.md) per impostare le dimensioni e la posizione della finestra. Per forzare il ricalcolo di questi attributi da parte di **Activatewindow** , chiamare prima il `CompleteConnect` metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




