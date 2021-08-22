---
description: Il metodo get \_ WindowState recupera lo stato della finestra corrente.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: CBaseControlWindow.get_WindowState metodo (Ctlutil.h)
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
ms.openlocfilehash: 5603e846fcf3357f01f896e6a0d34e34da6c355e5d41ab5d8f7b0c344c1a16dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586423"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a>Metodo CBaseControlWindow.get \_ WindowState

Il `get_WindowState` metodo recupera lo stato della finestra corrente.

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

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro restituisce un subset dei parametri della funzione **ShowWindow** di Microsoft Win32. In particolare, restituisce SW \_ SHOW e SW \_ HIDE, a seconda della visibilità corrente della finestra. Restituisce anche SW MINIMIZE e SW MAXIMIZE, a seconda che la finestra \_ sia \_ un'icona o sia espansa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




