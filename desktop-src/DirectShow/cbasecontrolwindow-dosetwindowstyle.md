---
description: Il metodo DoSetWindowStyle modifica gli stili di finestra tipici o estesi.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Metodo CBaseControlWindow. DoSetWindowStyle (Ctlutil. h)
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
ms.openlocfilehash: d57d023dff803caf5da7e61dea266670ec8bde5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325391"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>CBaseControlWindow. DoSetWindowStyle, metodo

Il `DoSetWindowStyle` metodo modifica gli stili di finestra tipici o estesi.

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



|              |                                      |
|--------------|--------------------------------------|
| \_stile GWL   | Recuperare gli stili della finestra.          |
| \_ExStyle GWL | Recuperare gli stili della finestra estesa. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro chiama la funzione **SetWindowLong** Win32 per impostare lo stile della finestra e quindi Visualizza nuovamente la finestra nella posizione corrente. Questa funzione membro viene chiamata dalle funzioni membro [**CBaseControlWindow::p UT \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) e [**CBaseControlWindow::p UT \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




