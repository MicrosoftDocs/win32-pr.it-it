---
description: Messaggio privato che imposta lo stile della finestra su WS ex in primo piano \_ \_ .
ms.assetid: 4934400e-4ca5-4ace-b9b9-3889f4cf610e
title: 'Membro CBaseWindow:: m_ShowStageTop (Winutil. h)'
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
ms.openlocfilehash: 8ed0069c5c65f2bb1a113c899e2d90de0cabcd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325776"
---
# <a name="cbasewindowm_showstagetop-member"></a>Membro ShowStageTop di CBaseWindow:: m \_

Messaggio privato che imposta lo stile della finestra su WS ex in primo piano \_ \_ .

## <a name="syntax"></a>Sintassi


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a>Osservazioni

I renderer video devono inviare questo messaggio alla finestra se passano alla modalità schermo intero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




