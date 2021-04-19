---
description: Il metodo PrepareWindow crea la finestra.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Metodo CBaseWindow. PrepareWindow (Winutil. h)
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
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332586"
---
# <a name="cbasewindowpreparewindow-method"></a>CBaseWindow. PrepareWindow, metodo

Il `PrepareWindow` metodo crea la finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                            | Descrizione         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Esito negativo.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo dopo avere creato l'oggetto. Questo metodo esegue una contabilità iniziale e quindi chiama il metodo [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) per creare la finestra.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




