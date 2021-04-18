---
description: Il \_ metodo Put FullScreenMode imposta la modalità a schermo intero del renderer.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: Metodo CBaseControlWindow.put_FullScreenMode (Ctlutil. h)
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
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328351"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a>CBaseControlWindow. put \_ FullScreenMode (metodo)

Il `put_FullScreenMode` metodo imposta la modalità a schermo intero del renderer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FullScreenMode* 
</dt> <dd>

Modalità schermo intero da applicare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . L'implementazione corrente restituisce E \_ NOTIMPL.

## <a name="remarks"></a>Commenti

Un renderer video che implementa una modalità a schermo intero deve eseguire l'override di questa funzione membro e implementare qualsiasi modalità supportata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




