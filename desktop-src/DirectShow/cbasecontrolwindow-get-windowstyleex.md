---
description: Il metodo get \_ WindowStyleEx recupera gli stili di finestra estesi.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: CBaseControlWindow.get_WindowStyleEx metodo (Ctlutil.h)
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
ms.openlocfilehash: 082b541c9f04122616f4f96548f1b1e58d940a6060fb4af1ac0fe51fa4887bb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331211"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a>Metodo CBaseControlWindow.get \_ WindowStyleEx

Il `get_WindowStyleEx` metodo recupera gli stili di finestra estesi.

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

Puntatore agli stili di finestra estesi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro recupera gli stili di finestra estesi. Chiama la [**funzione membro CBaseControlWindow::D oGetWindowStyle.**](cbasecontrolwindow-dogetwindowstyle.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




