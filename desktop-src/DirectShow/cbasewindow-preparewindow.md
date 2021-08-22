---
description: Il metodo PrepareWindow crea la finestra.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Metodo CBaseWindow.PrepareWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b2811e307b370323c331d3f894116ad0ff01af25ad76e1ea775dae5489dfb15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074565"
---
# <a name="cbasewindowpreparewindow-method"></a>Metodo CBaseWindow.PrepareWindow

Il `PrepareWindow` metodo crea la finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                            | Descrizione         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Esito negativo.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo dopo aver creato l'oggetto . Questo metodo esegue alcune operazioni iniziali di bookkeeping e quindi chiama il metodo [**CBaseWindow::D oCreateWindow**](cbasewindow-docreatewindow.md) per creare la finestra.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




