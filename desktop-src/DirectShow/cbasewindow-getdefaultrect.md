---
description: Il metodo GetDefaultRect recupera le dimensioni predefinite dell'area client.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Metodo CBaseWindow.GetDefaultRect (Winutil.h)
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
ms.openlocfilehash: e64d13a3fe77370d4b5bbefb7d493738b035c40ceebd13cd7f6f0f5c6d03f783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074615"
---
# <a name="cbasewindowgetdefaultrect-method"></a>Metodo CBaseWindow.GetDefaultRect

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

Quando la finestra viene attivata, l'oggetto chiama questo metodo per determinare le dimensioni dell'area client della finestra. Nella classe di base questo metodo restituisce un rettangolo la cui altezza e larghezza sono le costanti definite DEFHEIGHT e DEFWIDTH. Una classe derivata deve eseguire l'override di questo metodo. Per un renderer video, la classe derivata restituisce in genere le dimensioni dell'immagine video nativa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




