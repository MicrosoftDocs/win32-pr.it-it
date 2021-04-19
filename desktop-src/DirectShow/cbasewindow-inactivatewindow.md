---
description: Il metodo InactivateWindow disattiva la finestra. Nella classe di base, questo metodo nasconde la finestra.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Metodo CBaseWindow. InactivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1c5e925a3d9b510918636a221d5ad6e1b7da736
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327937"
---
# <a name="cbasewindowinactivatewindow-method"></a>CBaseWindow. InactivateWindow, metodo

Il `InactivateWindow` metodo disattiva la finestra. Nella classe di base, questo metodo nasconde la finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                    |
| <dl> <dt>**S \_ false**</dt> </dl> | La finestra è già inattiva.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




