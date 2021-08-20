---
description: Il metodo GetTargetRect recupera il rettangolo di destinazione corrente.
ms.assetid: b6542b06-af36-4666-b6fa-d9fa3c6c7044
title: Metodo CDrawImage.GetTargetRect (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ba520b0bb48ed60ba2a9c48165eb83959107ecd777bdecc8bce12e7672d221e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076411"
---
# <a name="cdrawimagegettargetrect-method"></a>Metodo CDrawImage.GetTargetRect

Il `GetTargetRect` metodo recupera il rettangolo di destinazione corrente.

## <a name="syntax"></a>Sintassi


```C++
void GetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Puntatore a una **struttura RECT** che riceve il rettangolo di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




