---
description: Il metodo SetDIBData specifica informazioni sulla bitmap indipendente dal dispositivo (DIB) GDI gestita da questo oggetto. Chiamare questo metodo per inizializzare l'oggetto CImageSample.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Metodo CImageSample. SetDIBData (Winutil. h)
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
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325048"
---
# <a name="cimagesamplesetdibdata-method"></a>CImageSample. SetDIBData, metodo

Il `SetDIBData` metodo specifica informazioni sulla bitmap indipendente dal dispositivo (DIB) GDI gestita da questo oggetto. Chiamare questo metodo per inizializzare l'oggetto **CImageSample** .

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

Puntatore a una struttura [**DIBDATA**](dibdata.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageSample**](cimagesample.md)
</dt> </dl>

 

 




