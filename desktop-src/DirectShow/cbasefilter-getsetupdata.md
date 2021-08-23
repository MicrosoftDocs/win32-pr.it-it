---
description: Il metodo GetSetupData recupera i dati di registrazione per il filtro.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Metodo CBaseFilter.GetSetupData (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f86bc35688ab0ec1c19053a95cbfd2025cf45ad666ef419fdb8440c6a844cb61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640471"
---
# <a name="cbasefiltergetsetupdata-method"></a>Metodo CBaseFilter.GetSetupData

Il `GetSetupData` metodo recupera i dati di registrazione per il filtro.

> [!Note]  
> Questo metodo è obsoleto. Viene chiamato dai metodi [**CBaseFilter::Register**](cbasefilter-register.md) e [**CBaseFilter::Unregister.**](cbasefilter-unregister.md)

 

## <a name="syntax"></a>Sintassi


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a una [**struttura AMOVIESETUP \_ FILTER**](amoviesetup-filter.md) contenente le informazioni di registrazione per il filtro.

## <a name="remarks"></a>Commenti

La classe base restituisce **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




