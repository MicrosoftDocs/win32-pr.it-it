---
description: Funzionalità di ricerca.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'Membro CSourceSeeking:: m_dwSeekingCaps (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329489"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a>Membro dwSeekingCaps di CSourceSeeking:: m \_

Funzionalità di ricerca.

## <a name="syntax"></a>Sintassi


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a>Osservazioni

Per impostazione predefinita, il valore è impostato sulla combinazione bit per bit dei flag seguenti:

-   \_Ricerca di \_ CanSeekForwards
-   \_Ricerca di \_ CanSeekBackwards
-   \_Ricerca di \_ CanSeekAbsolute
-   \_Ricerca di \_ CanGetStopPos
-   \_Ricerca di \_ CanGetDuration

Se il filtro supporta un set di funzionalità diverso, eseguire l'override di questo valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




