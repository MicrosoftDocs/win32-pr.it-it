---
description: Il metodo SetSubtype specifica il sottotipo.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Metodo CMediaType.SetSubtype (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96445074ce2f0cc5a27a4988087f2fd910444beca88e5dc89c84585a8a98b338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566371"
---
# <a name="cmediatypesetsubtype-method"></a>Metodo CMediaType.SetSubtype

Il `SetSubtype` metodo specifica il sottotipo.

## <a name="syntax"></a>Sintassi


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*psubtype* 
</dt> <dd>

Puntatore a **un GUID** che specifica il sottotipo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




