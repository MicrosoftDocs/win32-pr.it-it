---
description: Il metodo SetTemporalCompression specifica se gli esempi vengono compressi con la compressione temporale (interframe).
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Metodo CMediaType. SetTemporalCompression (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328503"
---
# <a name="cmediatypesettemporalcompression-method"></a>CMediaType. SetTemporalCompression, metodo

Il `SetTemporalCompression` metodo specifica se gli esempi vengono compressi con la compressione temporale (interframe).

## <a name="syntax"></a>Sintassi


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bCompressed* 
</dt> <dd>

Valore booleano che specifica se il flusso usa la compressione temporale. Se il flusso usa la compressione temporale, impostare il valore su **true**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo imposta il membro **bTemporalCompression** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




