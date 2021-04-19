---
description: "Il metodo senotify imposta o rimuove un callback nell'allocatore. L'allocatore chiama il metodo di callback ogni volta che viene chiamato il metodo IMemAllocator:: ReleaseBuffer dell'allocatore."
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Metodo CBaseAllocator. senotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331802"
---
# <a name="cbaseallocatorsetnotify-method"></a>Metodo CBaseAllocator. senotify

\[[**Senotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) può essere modificato o non disponibile nelle versioni successive.\]

Il `SetNotify` metodo imposta o rimuove un callback nell'allocatore. L'allocatore chiama il metodo di callback ogni volta che viene chiamato il metodo [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) dell'allocatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNotify* 
</dt> <dd>

Puntatore all'interfaccia [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) che verrà utilizzata per il callback. Il chiamante deve implementare l'interfaccia. Usare il valore **null** per rimuovere il callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo implementa il metodo [**IMemAllocatorCallbackTemp:: senotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) . L'allocatore non espone l'interfaccia [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) , a meno che il flag *fEnableReleaseCallback* non sia impostato su **true** nel costruttore [**CBaseAllocator**](cbaseallocator.md) .

Questo metodo imposta la variabile membro [**CBaseAllocator:: m \_ pNotify**](cbaseallocator-m-pnotify.md) uguale a *pNotify* e incrementa il conteggio dei riferimenti nell'interfaccia. Se *m \_ pNotify* è diverso da **null**, il metodo **ReleaseBuffer** dell'allocatore chiama [**IMemAllocatorNotifyCallbackTemp:: NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease). Per informazioni sull'implementazione del callback, vedere la sezione Osservazioni in questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




