---
description: Il metodo OnClose gestisce \_ i messaggi di chiusura WM.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Metodo CBaseWindow. OnClose (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325766"
---
# <a name="cbasewindowonclose-method"></a>Metodo CBaseWindow. OnClose

Il `OnClose` metodo gestisce \_ i messaggi di chiusura WM.

## <a name="syntax"></a>Sintassi


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true**.

## <a name="remarks"></a>Commenti

Nella classe di base, questo metodo nasconde semplicemente la finestra. In genere, una classe derivata eseguirà l'override di questo metodo in modo che invii anche un evento [**EC \_ USERABORT**](ec-userabort.md) . Non eseguire l'override del metodo per eliminare definitivamente la finestra. Al contrario, chiamare il metodo [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) quando il filtro proprietario viene eliminato definitivamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




