---
description: Il \_ metodo Put Visible consente di visualizzare o nascondere la finestra.
ms.assetid: 77e8d071-f876-4e35-945c-d1daf96ad02b
title: Metodo CBaseControlWindow.put_Visible (Ctlutil. h)
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
ms.openlocfilehash: 7bf713b4ccb9932b1201e7ced40fddcd87407ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333372"
---
# <a name="cbasecontrolwindowput_visible-method"></a>CBaseControlWindow. Put ( \_ metodo visibile)

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

Restituisce un valore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




