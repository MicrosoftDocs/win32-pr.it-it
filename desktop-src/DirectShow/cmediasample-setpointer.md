---
description: Il metodo setpoint imposta il puntatore sul buffer di memoria.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Metodo CMediaSample. sepointer (Amfilter. h)
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
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325310"
---
# <a name="cmediasamplesetpointer-method"></a>CMediaSample. setpoint, metodo

Il `SetPointer` metodo imposta il puntatore sul buffer di memoria.

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

Puntatore a un buffer di memoria allocato dal chiamante, di dimensioni *cBytes*.

</dd> <dt>

*cBytes* 
</dt> <dd>

Lunghezza del buffer, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo consente all'allocatore di impostare un nuovo puntatore per l'esempio.

Questo metodo non è disponibile tramite l'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . L'oggetto che crea l'esempio può accedere a questo metodo (tramite **CMediaSample**), ma gli altri oggetti non possono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




