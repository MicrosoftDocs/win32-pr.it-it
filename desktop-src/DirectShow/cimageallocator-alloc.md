---
description: Il metodo Alloc alloca memoria per i buffer. Questo metodo esegue l'override del metodo CBaseAllocator::Alloc.
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: Metodo CImageAllocator.Alloc (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bdf4c36bcf66d46a5c5ee7df16ac04a4461bd3a88de91e175b81e89ce496e1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076241"
---
# <a name="cimageallocatoralloc-method"></a>Metodo CImageAllocator.Alloc

Il `Alloc` metodo alloca memoria per i buffer. Questo metodo esegue l'override [**del metodo CBaseAllocator::Alloc.**](cbaseallocator-alloc.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                   | Descrizione                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione riuscita<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal metodo [**CBaseAllocator::Commit**](cbaseallocator-commit.md) quando il filtro esegue il commit dell'allocatore.

Questo metodo crea un elenco di esempi multimediali, implementati come [**oggetti CImageSample.**](cimagesample.md) Ogni esempio contiene una bitmap GDI indipendente dal dispositivo, usando la funzione **GDI CreateDIBSection.**

Internamente questo metodo chiama [**CImageAllocator::CreateDIB**](cimageallocator-createdib.md) per creare ogni DIB e [**CImageAllocator::CreateImageSample**](cimageallocator-createimagesample.md) per creare ogni esempio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




