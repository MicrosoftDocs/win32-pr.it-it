---
description: Il metodo get \_ FullScreenMode recupera la modalità schermo intero corrente.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: CBaseControlWindow.get_FullScreenMode metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cebd74fd51551249c339100ac2dd3eda4a171cc316cca575f27f5194480978ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660534"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a>Metodo CBaseControlWindow.get \_ FullScreenMode

Il `get_FullScreenMode` metodo recupera la modalità schermo intero corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Modalità schermo intero* 
</dt> <dd>

Puntatore alla modalità schermo intero corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro restituisce E \_ NOTIMPL per impostazione predefinita. In questo modo si informa il distributore del plug-in [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) che questo renderer non implementa un renderer a schermo intero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




