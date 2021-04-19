---
description: Il metodo DoGetWindowStyle recupera gli stili correnti della finestra normale o estesa.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Metodo CBaseControlWindow. DoGetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328095"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a>CBaseControlWindow. DoGetWindowStyle, metodo

Il `DoGetWindowStyle` metodo recupera gli stili correnti della finestra normale o estesa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStyle* 
</dt> <dd>

Puntatore a una variabile che riceve le informazioni sullo stile.

</dd> <dt>

*WindowLong* 
</dt> <dd>

Valore che specifica gli stili da recuperare. I possibili valori sono i seguenti:



|              |                                      |
|--------------|--------------------------------------|
| \_stile GWL   | Recuperare gli stili della finestra.          |
| \_ExStyle GWL | Recuperare gli stili della finestra estesa. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro chiama la funzione **GetWindowLong** Win32 per recuperare lo stile della finestra. Viene chiamato dalle funzioni membro [**CBaseControlWindow:: Get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) e [**CBaseControlWindow:: Get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




