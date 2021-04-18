---
description: Il metodo CreateDIB crea una bitmap (DIB) indipendente dal dispositivo GDI. Il valore DIB viene allocato in un blocco mempory condiviso, che elimina un'operazione di copia quando il filtro proprietario Blits l'immagine.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Metodo CImageAllocator. CreateDIB (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329772"
---
# <a name="cimageallocatorcreatedib-method"></a>CImageAllocator. CreateDIB, metodo

Il `CreateDIB` metodo crea una bitmap (DIB) indipendente dal dispositivo GDI. Il valore DIB viene allocato in un blocco mempory condiviso, che elimina un'operazione di copia quando il filtro proprietario Blits l'immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dimensioni* 
</dt> <dd>

Dimensione della bitmap.

</dd> <dt>

*DibData* \[ Ref\]
</dt> <dd>

Riferimento a una struttura [**DIBDATA**](dibdata.md) . Il metodo compila questa struttura con le informazioni sulla DIB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se l'esito è positivo o un codice di errore.

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

 

 




