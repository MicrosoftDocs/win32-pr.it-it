---
description: Il metodo CountSetBits restituisce il numero di bit impostato su 1 in un campo di bit specificato.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Metodo CImageDisplay. CountSetBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333077"
---
# <a name="cimagedisplaycountsetbits-method"></a>CImageDisplay. CountSetBits, metodo

Il `CountSetBits` metodo restituisce il numero di bit impostato su 1 in un campo di bit specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Campo* 
</dt> <dd>

Specifica un campo di bit come valore **DWORD** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di bit impostati su 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




