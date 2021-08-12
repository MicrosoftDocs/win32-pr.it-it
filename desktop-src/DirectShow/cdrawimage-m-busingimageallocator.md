---
description: La variabile \_ membro m bUsingImageAllocator indica se l'allocatore per la connessione pin è un oggetto CImageAllocator. Se il valore è TRUE, l'allocatore è un oggetto CImageAllocator (o derivato da tale classe).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: Membro CDrawImage::m_bUsingImageAllocator (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf60184758598872577e0c6b293f8eb0b72c5bf7305f1516a4dd6b5a4a639b94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657111"
---
# <a name="cdrawimagem_busingimageallocator-member"></a>Membro CDrawImage::m \_ bUsingImageAllocator

La `m_bUsingImageAllocator` variabile membro indica se l'allocatore per la connessione pin è un oggetto **CImageAllocator.** Se il valore è **TRUE,** l'allocatore è un **oggetto CImageAllocator** (o derivato da tale classe).

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a>Osservazioni

Quando il valore è **TRUE,** l'oggetto **CDrawImage** può usare le funzioni **GDI BitBlt** e **StretchBlt** per eseguire il rendering dell'immagine, anziché le funzioni **SetDIBitsToDevice** e **StretchDIBits** più lente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::NotifyAllocator**](cdrawimage-notifyallocator.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




