---
description: Metodo del costruttore.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Costruttore CMediaSample. CMediaSample (Amfilter. h)
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
ms.openlocfilehash: e4513af3b01d39f311fd1b8ecc1cea8f086d89c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326408"
---
# <a name="cmediasamplecmediasample-constructor"></a>Costruttore CMediaSample. CMediaSample

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

*pName* 
</dt> <dd>

Ignorato.

</dd> <dt>

*pAllocator* 
</dt> <dd>

Puntatore all'oggetto [**CBaseAllocator**](cbaseallocator.md) che ha creato l'esempio.

</dd> <dt>

*PHR* 
</dt> <dd>

Ignorato.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntatore a un buffer di memoria allocato dal chiamante, della *lunghezza* della dimensione.

</dd> <dt>

*length* 
</dt> <dd>

Lunghezza del buffer di memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe base non modifica il valore **HRESULT** passato nel parametro *PHR* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




