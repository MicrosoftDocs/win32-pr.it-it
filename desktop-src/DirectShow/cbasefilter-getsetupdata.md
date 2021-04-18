---
description: Il metodo GetSetupData recupera i dati di registrazione per il filtro.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Metodo CBaseFilter. GetSetupData (Amfilter. h)
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
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331548"
---
# <a name="cbasefiltergetsetupdata-method"></a>CBaseFilter. GetSetupData, metodo

Il `GetSetupData` metodo recupera i dati di registrazione per il filtro.

> [!Note]  
> Questo metodo è obsoleto. Viene chiamato dai metodi [**CBaseFilter:: Register**](cbasefilter-register.md) e [**CBaseFilter:: Unregister**](cbasefilter-unregister.md) .

 

## <a name="syntax"></a>Sintassi


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a una struttura di [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) contenente le informazioni di registrazione per il filtro.

## <a name="remarks"></a>Commenti

La classe base restituisce **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




