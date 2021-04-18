---
description: Flag che specifica se la finestra Invia o invia il messaggio di distruzione.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Membro CBaseWindow:: m_bDoPostToDestroy (Winutil. h)'
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
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330518"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a>Membro bDoPostToDestroy di CBaseWindow:: m \_

Flag che specifica se la finestra Invia o invia il messaggio di distruzione. Se **true**, il metodo [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) usa la funzione **PostMessage** per inviare a se stesso un messaggio di distruzione privata. Se **false**, **DoneWithWindow** utilizza la funzione **SendMessage** per inviare il messaggio. Per impostazione predefinita, il valore è **false**.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




