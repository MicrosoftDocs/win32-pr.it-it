---
description: Il \_ metodo get Left recupera la coordinata corrente della finestra a sinistra.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: Metodo CBaseControlWindow.get_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04f586cede24f8ff2017ae4004fc45c584a57f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331331"
---
# <a name="cbasecontrolwindowget_left-method"></a>Metodo CBaseControlWindow. Get \_ Left

Il `get_Left` metodo recupera la coordinata corrente della finestra a sinistra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pLeft* 
</dt> <dd>

Puntatore alla coordinata sinistra, espressa in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

La finestra è posizionata sul desktop. Questa posizione è espressa in pixel da quattro coordinate, a sinistra, in alto, a destra e in basso. Le interfacce automatizzate da OLE generalmente esprimono questa posizione attraverso Left, top, Width e Height. si tratta della convenzione usata in DirectShow. Tutte le coordinate sono espresse in pixel e la modifica di tutte le coordinate aggiornerà immediatamente la finestra.

L'impostazione delle coordinate di sinistra o superiore sposta la finestra verso l'alto e verso l'alto rispettivamente; Queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra. Analogamente, l'impostazione della larghezza e dell'altezza non ha alcun effetto sulle coordinate a sinistra e in alto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




