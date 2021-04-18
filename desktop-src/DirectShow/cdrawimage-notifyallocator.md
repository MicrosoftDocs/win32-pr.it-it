---
description: Il metodo NotifyAllocator informa l'oggetto CDrawImage se l'allocatore per la connessione è un oggetto CImageAllocator.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Metodo CDrawImage. NotifyAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331921"
---
# <a name="cdrawimagenotifyallocator-method"></a>CDrawImage. NotifyAllocator, metodo

Il `NotifyAllocator` metodo informa l'oggetto **CDrawImage** se l'allocatore per la connessione è un oggetto [**CImageAllocator**](cimageallocator.md) .

## <a name="syntax"></a>Sintassi


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bUsingImageAllocator* 
</dt> <dd>

Valore booleano che indica il tipo di allocatore usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il filtro proprietario deve chiamare questo metodo dopo che i pin accettano un allocatore. Se il filtro sa che l'allocatore è un oggetto **CImageAllocator** , deve chiamare questo metodo con il valore **true**. In genere, il filtro lo conoscerà solo se è proprietario dell'allocatore in questione. In caso contrario, deve chiamare questo metodo con il valore **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::D rawImage**](cdrawimage-drawimage.md)
</dt> </dl>

 

 




