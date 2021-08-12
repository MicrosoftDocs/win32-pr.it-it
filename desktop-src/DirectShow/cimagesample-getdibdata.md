---
description: Il metodo GetDIBData recupera informazioni sulla bitmap GDI indipendente dal dispositivo (DIB) che questo oggetto gestisce.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Metodo CImageSample.GetDIBData (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 894d75512c6c7909f617e13999e7290efea663fa843bf64424aad8371965de75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655600"
---
# <a name="cimagesamplegetdibdata-method"></a>Metodo CImageSample.GetDIBData

Il metodo recupera informazioni sulla bitmap GDI indipendente dal dispositivo `GetDIBData` (DIB) che questo oggetto gestisce.

## <a name="syntax"></a>Sintassi


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a una [**struttura DIBDATA.**](dibdata.md)

## <a name="remarks"></a>Commenti

Il chiamante deve inizializzare **la struttura DIBDATA** prima di chiamare questo metodo. controllare il valore di **CImageSample::m \_ bInit**. Per inizializzare la struttura, chiamare il [**metodo CImageSample::SetDIBData.**](cimagesample-setdibdata.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageSample**](cimagesample.md)
</dt> </dl>

 

 




