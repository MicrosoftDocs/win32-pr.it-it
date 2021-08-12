---
description: Il metodo ReleaseBuffer restituisce un esempio multimediale all'elenco di esempi di supporti gratuiti. Questo metodo implementa il metodo IMemAllocator::ReleaseBuffer.
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Metodo CBaseAllocator.ReleaseBuffer (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d1096cc7cd4ed31346b38719a3f622edf780408fd50262d93515f68d92b421d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661507"
---
# <a name="cbaseallocatorreleasebuffer-method"></a>Metodo CBaseAllocator.ReleaseBuffer

Il `ReleaseBuffer` metodo restituisce un esempio multimediale all'elenco di esempi di supporti gratuiti. Questo metodo implementa il [**metodo IMemAllocator::ReleaseBuffer.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'oggetto di esempio multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Quando il conteggio dei riferimenti di un campione multimediale raggiunge lo zero, l'esempio chiama **ReleaseBuffer** con se stesso come parametro. Questo metodo esegue le azioni seguenti.

-   Restituisce l'esempio multimediale all'elenco libero ([**CBaseAllocator::m \_ lFree**](cbaseallocator-m-lfree.md)).
-   Chiama il [**metodo CBaseAllocator::NotifySample,**](cbaseallocator-notifysample.md) che rilascia tutti i thread bloccati nelle chiamate al [**metodo CBaseAllocator::GetBuffer.**](cbaseallocator-getbuffer.md)
-   Se il [**metodo CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) è stato chiamato in precedenza, chiama il metodo **IMemAllocatorNotifyCallbackTemp::NotifyRelease.**
-   Quando viene rilasciato l'ultimo esempio, se è presente una chiamata [**CBaseAllocator::D ecommit in**](cbaseallocator-decommit.md) sospeso, chiama il metodo [**CBaseAllocator::Free**](cbaseallocator-free.md) per rilasciare la memoria buffer. Nella classe di base **Free è** un metodo virtuale puro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




