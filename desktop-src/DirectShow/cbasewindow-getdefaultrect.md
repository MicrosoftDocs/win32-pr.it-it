---
description: Il metodo GetDefaultRect recupera le dimensioni predefinite dell'area client.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Metodo CBaseWindow. GetDefaultRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327944"
---
# <a name="cbasewindowgetdefaultrect-method"></a>CBaseWindow. GetDefaultRect, metodo

Il `GetDefaultRect` metodo recupera le dimensioni predefinite dell'area client.

## <a name="syntax"></a>Sintassi


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il rettangolo predefinito.

## <a name="remarks"></a>Commenti

Quando la finestra viene attivata, l'oggetto chiama questo metodo per determinare la dimensione che deve rendere l'area client della finestra. Nella classe di base, questo metodo restituisce un rettangolo la cui altezza e larghezza sono le costanti definite DEFHEIGHT e DEFWIDTH. Una classe derivata deve eseguire l'override di questo metodo. Per un renderer video, la classe derivata restituirà in genere le dimensioni dell'immagine video nativa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




