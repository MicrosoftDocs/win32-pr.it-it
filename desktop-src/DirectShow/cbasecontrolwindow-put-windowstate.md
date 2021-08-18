---
description: Il metodo put \_ WindowState imposta lo stato della finestra.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: CBaseControlWindow.put_WindowState metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4769aff01c251017734fd7152fa703cd51064db11fb91851fd0b8fed76fc3d96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635701"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a>Metodo CBaseControlWindow.put \_ WindowState

Il `put_WindowState` metodo imposta lo stato della finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Windowstate* 
</dt> <dd>

Nuovo stato della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro accetta gli stessi parametri della funzione Microsoft Win32 **ShowWindow** ,ad esempio WS \_ SHOWNORMAL, WS \_ SHOWMINNOACTIVATE e WS \_ SHOWMAXIMIZED.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




