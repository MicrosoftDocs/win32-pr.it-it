---
description: Recupera l'oggetto FOURCC&\# 160;DWORD dall'oggetto FOURCCMap.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: Metodo FOURCCMap::GetFOURCC (Fourcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 381625f5d0a585f212c8f7b076d1cd58ea5215958bf09025e1db864ce2f624b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015719"
---
# <a name="fourccmapgetfourcc-method"></a>Metodo FOURCCMap::GetFOURCC

Recupera il **valore DWORD FOURCC**  dall'oggetto [**FOURCCMap.**](fourccmap.md)

## <a name="syntax"></a>Sintassi


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il **valore DWORD FOURCC.**  Si noti che se si costruisce **un GUID** che non è stato originariamente derivato da **fourcc,** il valore restituito sarà essenzialmente casuale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Fourcc.h (include Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 




