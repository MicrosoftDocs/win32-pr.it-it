---
description: Il metodo put \_ Visible consente di visualizzare o nascondere la finestra.
ms.assetid: 77e8d071-f876-4e35-945c-d1daf96ad02b
title: CBaseControlWindow.put_Visible metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2c8565d14c58d520a91c682e55d3dbc2ba079cf956213bdc61d044834d690c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793291"
---
# <a name="cbasecontrolwindowput_visible-method"></a>Metodo CBaseControlWindow.put \_ Visible

Il `put_Visible` metodo consente di visualizzare o nascondere la finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Visible(
   long Visible
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Visible* 
</dt> <dd>

Flag booleano di automazione (0 indica che la finestra è nascosta, 1 indica che la finestra è visualizzata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




