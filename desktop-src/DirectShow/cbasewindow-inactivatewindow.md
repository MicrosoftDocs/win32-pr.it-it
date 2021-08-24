---
description: Il metodo InactivateWindow attiva la finestra. Nella classe di base questo metodo nasconde la finestra.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Metodo CBaseWindow.InactivateWindow (Winutil.h)
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
ms.openlocfilehash: 3cf175a55ab5739b0fa171fe4c9553d3691be82d71b38fd5eb480d6e28043440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567461"
---
# <a name="cbasewindowinactivatewindow-method"></a>Metodo CBaseWindow.InactivateWindow

Il `InactivateWindow` metodo disattiva la finestra. Nella classe di base questo metodo nasconde la finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                    |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | La finestra è già inattiva.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




