---
description: Il metodo DoSetWindowStyle modifica gli stili di finestra tipici o estesi.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Metodo CBaseControlWindow.DoSetWindowStyle (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db88c5818d31d65f361ae1a805bd50c285d4a5c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909809"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>Metodo CBaseControlWindow.DoSetWindowStyle

Il metodo modifica gli stili di finestra tipici `DoSetWindowStyle` o estesi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Style* 
</dt> <dd>

Stili di finestra appropriati.

</dd> <dt>

*WindowLong* 
</dt> <dd>

Valore che specifica gli stili da impostare. I possibili valori sono i seguenti:



| Label | Valore |
|--------------|--------------------------------------|
| STILE \_ GWL   | Recuperare gli stili della finestra.          |
| GWL \_ EXSTYLE | Recuperare gli stili di finestra estesi. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro chiama la funzione **Win32 SetWindowLong** per impostare lo stile della finestra e quindi visualizza nuovamente la finestra nella posizione corrente. Questa funzione membro viene chiamata dalle funzioni membro [**CBaseControlWindow::p ut \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) e [**CBaseControlWindow::p ut \_ WindowStyleEx.**](cbasecontrolwindow-put-windowstyleex.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




