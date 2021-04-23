---
description: Il metodo DoGetWindowStyle recupera gli stili di finestra normali o estesi correnti.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Metodo CBaseControlWindow.DoGetWindowStyle (Ctlutil.h)
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
ms.openlocfilehash: d970ee52203c5c8dfe8a897c5612604becc2b2e1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909819"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a>Metodo CBaseControlWindow.DoGetWindowStyle

Il `DoGetWindowStyle` metodo recupera gli stili di finestra normali o estesi correnti.

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



| Label | Valore |
|--------------|--------------------------------------|
| STILE \_ GWL   | Recuperare gli stili della finestra.          |
| GWL \_ EXSTYLE | Recuperare gli stili di finestra estesi. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro chiama la funzione Win32 **GetWindowLong** per recuperare lo stile della finestra. Viene chiamato dalle funzioni membro [**CBaseControlWindow::get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) e [**CBaseControlWindow::get \_ WindowStyleEx.**](cbasecontrolwindow-get-windowstyleex.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




