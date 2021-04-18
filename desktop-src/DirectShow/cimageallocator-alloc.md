---
description: "Il metodo Alloc alloca memoria per i buffer. Questo metodo esegue l'override del metodo CBaseAllocator:: Alloc."
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: Metodo CImageAllocator. Alloc (Winutil. h)
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
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329775"
---
# <a name="cimageallocatoralloc-method"></a>CImageAllocator. Alloc, metodo

Il `Alloc` metodo alloca memoria per i buffer. Questo metodo esegue l'override del metodo [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                   | Descrizione                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione riuscita<br/>             |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal metodo [**CBaseAllocator:: commit**](cbaseallocator-commit.md) , quando il filtro esegue il commit dell'allocatore.

Questo metodo crea un elenco di esempi di supporti, implementati come oggetti [**CImageSample**](cimagesample.md) . Ogni esempio contiene una bitmap indipendente dal dispositivo GDI, usando la funzione **CreateDIBSection** di GDI.

Internamente questo metodo chiama [**CImageAllocator:: CreateDIB**](cimageallocator-createdib.md) per creare ogni DIB e [**CImageAllocator:: CreateImageSample**](cimageallocator-createimagesample.md) per creare ogni campione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




