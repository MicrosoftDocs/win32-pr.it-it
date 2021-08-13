---
description: Il metodo ActivateWindow ridimensiona la finestra in base ai requisiti della classe derivata.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Metodo CBaseWindow.ActivateWindow (Winutil.h)
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
ms.openlocfilehash: e00c3ccc43e2583ce8664e62967a22f753148cfa271dd1995e2374c2bfa53c71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658245"
---
# <a name="cbasewindowactivatewindow-method"></a>Metodo CBaseWindow.ActivateWindow

Il `ActivateWindow` metodo ridimensiona la finestra in base ai requisiti della classe derivata.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Finestra già attivata.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                      |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il [**metodo CBaseWindow::GetDefaultRect**](cbasewindow-getdefaultrect.md) per determinare le dimensioni della finestra. La classe derivata deve eseguire **l'override di GetDefaultRect** per restituire le dimensioni delle immagini che verranno visualizzate.

Se la finestra è già attiva, la chiamata di sposta la finestra nella parte superiore dell'ordine Z, ma `ActivateWindow` non ridimensiona la finestra. Lo stesso vale se la finestra ha un elemento padre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




