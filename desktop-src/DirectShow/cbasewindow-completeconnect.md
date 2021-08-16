---
description: Il metodo CompleteConnect notifica alla finestra che il pin di input del renderer è stato connesso.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Metodo CBaseWindow.CompleteConnect (Winutil.h)
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
ms.openlocfilehash: 5e04e0adf1d11a4878d860dd5c8a1eea9395095c71d8b5c86d6023a24ccdb28c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016709"
---
# <a name="cbasewindowcompleteconnect-method"></a>Metodo CBaseWindow.CompleteConnect

Il metodo notifica alla finestra che il pin di input del `CompleteConnect` renderer è stato connesso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo reimposta il flag di attivazione della finestra ([**CBaseWindow::m \_ bActivated**](cbasewindow-m-bactivated.md)) su **FALSE.** Quando un renderer video completa una connessione pin, potrebbe chiamare il metodo [**CBaseWindow::ActivateWindow**](cbasewindow-activatewindow.md) per impostare le dimensioni e la posizione della finestra. Per **forzare ActivateWindow** a ricalcolare questi attributi, chiamare prima il `CompleteConnect` metodo .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




