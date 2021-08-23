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
ms.openlocfilehash: d3b1f72ace792f13f88fbf0ce1e0edaf7b08789ecba88aede0b4094e9e75ae52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640882"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>Metodo CBaseControlWindow.DoSetWindowStyle

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



| Etichetta | Valore |
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
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




