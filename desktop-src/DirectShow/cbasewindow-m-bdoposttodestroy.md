---
description: Flag che specifica se la finestra invia o invia il messaggio di distruzione.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: Membro CBaseWindow::m_bDoPostToDestroy (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 070b94cc75fa3fb2d9b5983901abc2406b2e601ec3370323854905708ee681f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954610"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a>Membro CBaseWindow::m \_ bDoPostToDestroy

Flag che specifica se la finestra invia o invia il messaggio di distruzione. Se **TRUE,** il [**metodo CBaseWindow::D oneWithWindow**](cbasewindow-donewithwindow.md) usa la **funzione PostMessage** per inviare a se stesso un messaggio di distruzione privato. Se **FALSE,** **DoneWithWindow** usa la **funzione SendMessage** per inviare il messaggio. Per impostazione predefinita, il valore è **FALSE.**

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




