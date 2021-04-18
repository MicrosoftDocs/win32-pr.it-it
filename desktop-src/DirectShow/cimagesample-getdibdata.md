---
description: Il metodo GetDIBData recupera le informazioni sulla bitmap indipendente dal dispositivo (DIB) GDI gestita da questo oggetto.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Metodo CImageSample. GetDIBData (Winutil. h)
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
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325055"
---
# <a name="cimagesamplegetdibdata-method"></a>CImageSample. GetDIBData, metodo

Il `GetDIBData` metodo recupera le informazioni sulla bitmap indipendente dal dispositivo (DIB) GDI gestita da questo oggetto.

## <a name="syntax"></a>Sintassi


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a una struttura [**DIBDATA**](dibdata.md) .

## <a name="remarks"></a>Commenti

Il chiamante deve inizializzare la struttura **DIBDATA** prima di chiamare questo metodo. verificare il valore di **CImageSample:: m \_ Binit**. Per inizializzare la struttura, chiamare il metodo [**CImageSample:: SetDIBData**](cimagesample-setdibdata.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageSample**](cimagesample.md)
</dt> </dl>

 

 




