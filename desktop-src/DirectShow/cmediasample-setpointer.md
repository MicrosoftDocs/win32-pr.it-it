---
description: Il metodo SetPointer imposta il puntatore al buffer di memoria.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Metodo CMediaSample.SetPointer (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af6747eb9ed39a973d795d8701fd9d7afd1b88e9d0b0db577de6a8e963b840bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634351"
---
# <a name="cmediasamplesetpointer-method"></a>Metodo CMediaSample.SetPointer

Il `SetPointer` metodo imposta il puntatore al buffer di memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ptr* 
</dt> <dd>

Puntatore a un buffer di memoria allocato dal chiamante, di *dimensioni cByte.*

</dd> <dt>

*cByte* 
</dt> <dd>

Lunghezza del buffer, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo consente all'allocatore di impostare un nuovo puntatore per l'esempio.

Questo metodo non è disponibile tramite [**l'interfaccia IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample) L'oggetto che crea l'esempio può accedere a questo metodo (tramite **CMediaSample),** ma altri oggetti non possono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




