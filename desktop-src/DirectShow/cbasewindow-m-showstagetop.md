---
description: Messaggio privato che imposta lo stile della finestra su WS \_ EX \_ TOPMOST.
ms.assetid: 4934400e-4ca5-4ace-b9b9-3889f4cf610e
title: Membro CBaseWindow::m_ShowStageTop (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ShowStageTop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dbd8943b297d6e33f3b86a62c7e67dd2039a6b99d316061be30a4c3016711c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016519"
---
# <a name="cbasewindowm_showstagetop-member"></a>Membro CBaseWindow::m \_ ShowStageTop

Messaggio privato che imposta lo stile della finestra su WS \_ EX \_ TOPMOST.

## <a name="syntax"></a>Sintassi


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a>Osservazioni

I renderer video devono inviare questo messaggio alla finestra se passano alla modalità schermo intero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




