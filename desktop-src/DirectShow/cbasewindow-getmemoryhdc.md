---
description: Il metodo GetMemoryHDC recupera un handle per il contesto di dispositivo di memoria.
ms.assetid: 2c22015f-5948-4e1a-92c7-36f232816175
title: Metodo CBaseWindow.GetMemoryHDC (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetMemoryHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36874817d2e1dd13c00577a91cff7f059c1f2441701012af202c4765cb23088a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016659"
---
# <a name="cbasewindowgetmemoryhdc-method"></a>Metodo CBaseWindow.GetMemoryHDC

Il `GetMemoryHDC` metodo recupera un handle per il contesto di dispositivo (DC) della memoria.

## <a name="syntax"></a>Sintassi


```C++
virtual HDC GetMemoryHDC();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un handle al controller di dominio di memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




