---
description: Il metodo GetPointer recupera un puntatore di lettura/scrittura al buffer. Questo metodo implementa il metodo IMediaSample::GetPointer.
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Metodo CMediaSample.GetPointer (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21a39fae4f243c0a4e7305573f1b06ee2f11766729ef4933124d059b20b3a14b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832271"
---
# <a name="cmediasamplegetpointer-method"></a>Metodo CMediaSample.GetPointer

Il `GetPointer` metodo recupera un puntatore di lettura/scrittura al buffer. Questo metodo implementa il [**metodo IMediaSample::GetPointer.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppBuffer* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore al buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




