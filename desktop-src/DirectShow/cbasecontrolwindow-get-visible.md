---
description: Il \_ metodo get Visible recupera la visibilità della finestra corrente.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: Metodo CBaseControlWindow.get_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332351"
---
# <a name="cbasecontrolwindowget_visible-method"></a>CBaseControlWindow. Get ( \_ metodo visibile)

Il `get_Visible` metodo recupera la visibilità della finestra corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVisible* 
</dt> <dd>

Puntatore a un flag booleano di automazione (0 è disattivato, 1 è on).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro restituisce 1 se la finestra ha lo stile di visualizzazione WS \_ ; in caso contrario, 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




