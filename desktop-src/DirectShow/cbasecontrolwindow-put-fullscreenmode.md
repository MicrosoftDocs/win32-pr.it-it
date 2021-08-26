---
description: Il metodo \_ put FullScreenMode imposta la modalità schermo intero del renderer.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: CBaseControlWindow.put_FullScreenMode metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e7aa121ce78198fe6b2ca0b88109183665f0cd93dd95294a848a2b2d0c03548
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983681"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a>Metodo CBaseControlWindow.put \_ FullScreenMode

Il `put_FullScreenMode` metodo imposta la modalità schermo intero del renderer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Modalità schermo intero* 
</dt> <dd>

Modalità schermo intero da applicare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** L'implementazione corrente restituisce E \_ NOTIMPL.

## <a name="remarks"></a>Commenti

Un renderer video che implementa una modalità schermo intero deve eseguire l'override di questa funzione membro e implementare le modalità supportate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




