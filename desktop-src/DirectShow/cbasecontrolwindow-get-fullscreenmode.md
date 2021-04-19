---
description: Il \_ metodo Get FullScreenMode recupera la modalità a schermo intero corrente.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: Metodo CBaseControlWindow.get_FullScreenMode (Ctlutil. h)
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
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329869"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a>Metodo CBaseControlWindow. Get \_ FullScreenMode

Il `get_FullScreenMode` metodo recupera la modalità a schermo intero corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FullScreenMode* 
</dt> <dd>

Puntatore alla modalità a schermo intero corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro restituisce E \_ NOTIMPL per impostazione predefinita. In questo modo si informa il server di distribuzione plug-in [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) che questo renderer non implementa un renderer a schermo intero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




