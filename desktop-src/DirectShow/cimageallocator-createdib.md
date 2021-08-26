---
description: Il metodo CreateDIB crea una bitmap GDI indipendente dal dispositivo (DIB). Il dib viene allocato in un blocco mempory condiviso, che elimina un'operazione di copia quando il filtro proprietario copia l'immagine.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Metodo CImageAllocator.CreateDIB (Winutil.h)
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
ms.openlocfilehash: 94a629831ea50219b47500c0637cfeaebfbc95b1ee99a8b9d3872a655ab5485c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055481"
---
# <a name="cimageallocatorcreatedib-method"></a>Metodo CImageAllocator.CreateDIB

Il `CreateDIB` metodo crea una bitmap GDI indipendente dal dispositivo (DIB). Il dib viene allocato in un blocco mempory condiviso, che elimina un'operazione di copia quando il filtro proprietario copia l'immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InSize* 
</dt> <dd>

Dimensioni della bitmap.

</dd> <dt>

*DibData* \[ Ref\]
</dt> <dd>

Riferimento a una [**struttura DIBDATA.**](dibdata.md) Il metodo inserisce questa struttura con informazioni sul dib.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo oppure un codice di errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator::Alloc**](cimageallocator-alloc.md)
</dt> </dl>

 

 




