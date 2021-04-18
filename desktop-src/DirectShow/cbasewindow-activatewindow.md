---
description: Il metodo ActivateWindow ridimensiona la finestra in base ai requisiti della classe derivata.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Metodo CBaseWindow. ActivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330524"
---
# <a name="cbasewindowactivatewindow-method"></a>CBaseWindow. ActivateWindow, metodo

Il `ActivateWindow` metodo ridimensiona la finestra in base ai requisiti della classe derivata.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | La finestra è già stata attivata.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                      |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CBaseWindow:: GetDefaultRect**](cbasewindow-getdefaultrect.md) per determinare le dimensioni della finestra. La classe derivata deve eseguire l'override di **GetDefaultRect** per restituire la dimensione delle immagini che verranno visualizzate.

Se la finestra è già attiva, la chiamata `ActivateWindow` Sposta la finestra nella parte superiore del z order, ma non ridimensiona la finestra. Lo stesso vale se la finestra dispone di un elemento padre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




