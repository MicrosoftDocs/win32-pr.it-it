---
description: 'Costruttore CMediaSample.CMediaSample : metodo costruttore.'
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Costruttore CMediaSample.CMediaSample (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5baa5b791078eaf292b8da89fe50adaf7de9172185f8e6cab8745781030f401f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634691"
---
# <a name="cmediasamplecmediasample-constructor"></a>Costruttore CMediaSample.CMediaSample

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Ignorato.

</dd> <dt>

*pAllocator* 
</dt> <dd>

Puntatore [**all'oggetto CBaseAllocator**](cbaseallocator.md) che ha creato questo esempio.

</dd> <dt>

*Phr* 
</dt> <dd>

Ignorato.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntatore a un buffer di memoria allocato dal chiamante, di lunghezza *.*

</dd> <dt>

*length* 
</dt> <dd>

Lunghezza del buffer di memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe base non modifica il **valore HRESULT** passato nel *parametro phr.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




