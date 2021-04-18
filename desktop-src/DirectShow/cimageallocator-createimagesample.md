---
description: Il metodo CreateImageSample crea un esempio di supporto.
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: Metodo CImageAllocator. CreateImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329771"
---
# <a name="cimageallocatorcreateimagesample-method"></a>CImageAllocator. CreateImageSample, metodo

Il `CreateImageSample` metodo crea un esempio di supporto.

## <a name="syntax"></a>Sintassi


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Puntatore a un buffer di *lunghezza* di dimensione, allocato dal chiamante.

</dd> <dt>

*Length* 
</dt> <dd>

Lunghezza del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un oggetto [**CImageSample**](cimagesample.md) .

## <a name="remarks"></a>Commenti

Questo metodo crea un nuovo esempio di supporto, implementato come oggetto **CImageSample** . Il metodo [**IMediaSample:: Getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) dell'esempio restituisce un puntatore al buffer specificato nel parametro *pData* .

Se si deriva una nuova classe allocator da [**CImageAllocator**](cimageallocator.md) e una nuova classe di esempio media da [**CImageSample**](cimagesample.md), è necessario eseguire l'override di questo metodo per creare un'istanza della classe di esempio multimediale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator:: Alloc**](cimageallocator-alloc.md)
</dt> </dl>

 

 




