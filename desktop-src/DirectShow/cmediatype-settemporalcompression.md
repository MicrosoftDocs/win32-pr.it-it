---
description: Il metodo SetTemporalCompression specifica se i campioni vengono compressi usando la compressione temporale (interframe).
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Metodo CMediaType.SetTemporalCompression (Mtype.h)
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
ms.openlocfilehash: d29efb0ec16f99c7354621bc49bd36c4e367375d5eb68a2d94a69c27bfdce2f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954400"
---
# <a name="cmediatypesettemporalcompression-method"></a>Metodo CMediaType.SetTemporalCompression

Il `SetTemporalCompression` metodo specifica se i campioni vengono compressi usando la compressione temporale (interframe).

## <a name="syntax"></a>Sintassi


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*b Compresso* 
</dt> <dd>

Valore booleano che specifica se il flusso usa la compressione temporale. Se il flusso usa la compressione temporale, impostare il valore su **TRUE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo imposta il **membro bTemporalCompression.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




