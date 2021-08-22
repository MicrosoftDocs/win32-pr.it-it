---
description: Il metodo SetDIBData specifica informazioni sulla bitmap GDI indipendente dal dispositivo (DIB) che questo oggetto gestisce. Chiamare questo metodo per inizializzare l'oggetto CImageSample.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Metodo CImageSample.SetDIBData (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367fed37545e9498f9f6e753a57a7eeeb2ce8767779241284be9109676fafd38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655525"
---
# <a name="cimagesamplesetdibdata-method"></a>Metodo CImageSample.SetDIBData

Il metodo specifica informazioni sulla bitmap GDI indipendente dal dispositivo `SetDIBData` (DIB) che questo oggetto gestisce. Chiamare questo metodo per inizializzare **l'oggetto CImageSample.**

## <a name="syntax"></a>Sintassi


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDibData* 
</dt> <dd>

Puntatore a [**una struttura DIBDATA.**](dibdata.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageSample**](cimagesample.md)
</dt> </dl>

 

 




