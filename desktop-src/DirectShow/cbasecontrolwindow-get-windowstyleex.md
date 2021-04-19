---
description: Il \_ metodo Get WindowStyleEx recupera gli stili della finestra estesa.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: Metodo CBaseControlWindow.get_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c59336ab57e92e99366494a272f2b995191b494b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332346"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a>Metodo CBaseControlWindow. Get \_ WindowStyleEx

Il `get_WindowStyleEx` metodo recupera gli stili della finestra estesa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWindowStyleEx* 
</dt> <dd>

Puntatore agli stili della finestra estesa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro recupera gli stili della finestra estesa. Chiama la funzione membro [**CBaseControlWindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




