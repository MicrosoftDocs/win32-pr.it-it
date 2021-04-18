---
description: "Il metodo ReleaseBuffer restituisce un esempio di supporto all'elenco di esempi di supporti disponibili. Questo metodo implementa il metodo IMemAllocator:: ReleaseBuffer."
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Metodo CBaseAllocator. ReleaseBuffer (Amfilter. h)
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
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331804"
---
# <a name="cbaseallocatorreleasebuffer-method"></a>CBaseAllocator. ReleaseBuffer, metodo

Il `ReleaseBuffer` metodo restituisce un esempio di supporto all'elenco di esempi di supporti disponibili. Questo metodo implementa il metodo [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .

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

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'oggetto di esempio multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Quando il conteggio dei riferimenti di un campione multimediale raggiunge zero, l'esempio chiama **ReleaseBuffer** con se stesso come parametro. Questo metodo esegue le azioni seguenti.

-   Restituisce l'esempio di supporto all'elenco di disponibilità ([**CBaseAllocator:: m \_ lFree**](cbaseallocator-m-lfree.md)).
-   Chiama il metodo [**CBaseAllocator:: NotifySample**](cbaseallocator-notifysample.md) , che rilascia tutti i thread bloccati sulle chiamate al metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) .
-   Se il metodo [**CBaseAllocator:: senotify**](cbaseallocator-setnotify.md) è stato chiamato in precedenza, chiama il metodo **IMemAllocatorNotifyCallbackTemp:: NotifyRelease** .
-   Quando viene rilasciato l'ultimo esempio, se è presente una chiamata a [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) in sospeso, chiama il metodo [**CBaseAllocator:: Free**](cbaseallocator-free.md) per rilasciare la memoria del buffer. Nella classe di base, **Free** è un metodo virtuale puro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




