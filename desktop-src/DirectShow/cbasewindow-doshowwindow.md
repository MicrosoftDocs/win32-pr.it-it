---
description: Il metodo DoShowWindow imposta lo stato di visualizzazione della finestra.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Metodo CBaseWindow.DoShowWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fef63e04d0e04f2fe0daa78cd6b33a22fa7c8fa14c57b1e022703dea0914dab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074630"
---
# <a name="cbasewindowdoshowwindow-method"></a>Metodo CBaseWindow.DoShowWindow

Il **metodo DoShowWindow** imposta lo stato di visualizzazione della finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ShowCmd* 
</dt> <dd>

Flag che specifica la modalità di visualizzazione della finestra. Il valore può essere qualsiasi costante definita per il *parametro nCmdShow* della [**funzione ShowWindow.**](/windows/desktop/api/winuser/nf-winuser-showwindow)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

