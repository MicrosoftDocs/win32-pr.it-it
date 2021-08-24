---
description: Recupera le dimensioni massime in byte necessarie per il flusso corrente, incluso il numero di versione.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Metodo CPersistStream.GetSizeMax (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 746fb01102642f2d3e6b254ac741c284143aaecfd401fc220bf7a9d97d93e64e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813371"
---
# <a name="cpersiststreamgetsizemax-method"></a>Metodo CPersistStream.GetSizeMax

Recupera le dimensioni massime in byte necessarie per il flusso corrente, incluso il numero di versione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcbSize* 
</dt> <dd>

Puntatore alla dimensione in byte necessaria per salvare il flusso, incluso il numero di versione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il **metodo IPersistStream::GetSizeMax.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pstream.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




