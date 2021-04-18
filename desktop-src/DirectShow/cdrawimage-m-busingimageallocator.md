---
description: La \_ variabile membro bUsingImageAllocator m indica se l'allocatore per la connessione pin è un oggetto CImageAllocator. Se il valore è TRUE, l'allocatore è un oggetto CImageAllocator (o deriva da tale classe).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Membro CDrawImage:: m_bUsingImageAllocator (Winutil. h)'
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
ms.openlocfilehash: e08d1e8217f42c6855759cefeef40e56949156fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330682"
---
# <a name="cdrawimagem_busingimageallocator-member"></a>Membro bUsingImageAllocator di CDrawImage:: m \_

La `m_bUsingImageAllocator` variabile membro indica se l'allocatore per la connessione pin è un oggetto **CImageAllocator** . Se il valore è **true**, l'allocatore è un oggetto **CImageAllocator** (o deriva da tale classe).

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a>Osservazioni

Quando il valore è **true**, l'oggetto **CDrawImage** può utilizzare le funzioni **GDI BitBlt** e **StretchBlt** per eseguire il rendering dell'immagine, anziché le funzioni più lente **SetDIBitsToDevice** e **StretchDIBits** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::NotifyAllocator**](cdrawimage-notifyallocator.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




