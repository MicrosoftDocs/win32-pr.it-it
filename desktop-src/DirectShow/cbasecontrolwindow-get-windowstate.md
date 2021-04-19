---
description: Il \_ metodo get WindowState recupera lo stato corrente della finestra.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: Metodo CBaseControlWindow.get_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332348"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a>Metodo CBaseControlWindow. Get \_ WindowState

Il `get_WindowState` metodo recupera lo stato corrente della finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWindowState* 
</dt> <dd>

Puntatore allo stato della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro restituisce un subset dei parametri della funzione **ShowWindow** di Microsoft Win32. In particolare, restituisce SW \_ Show e SW \_ Hide, a seconda della visibilità corrente della finestra. Restituisce inoltre SW \_ Riduci a icona e SW \_ ingrandito, a seconda che la finestra sia un'icona o espansa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




