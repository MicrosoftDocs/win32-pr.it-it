---
description: Il metodo SetStretchMode calcola se l'immagine video deve essere estesa.
ms.assetid: ffdcaf9c-e157-4557-9193-8430c1c451bf
title: Metodo CDrawImage.SetStretchMode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetStretchMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3886910bce57aca728f64ffbe9d660c1073d1281864a7721faa7e757c7c7d81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526491"
---
# <a name="cdrawimagesetstretchmode-method"></a>Metodo CDrawImage.SetStretchMode

Il `SetStretchMode` metodo calcola se l'immagine video deve essere estesa.

## <a name="syntax"></a>Sintassi


```C++
void SetStretchMode();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La **classe CDrawImage** chiama automaticamente questo metodo ogni volta che il rettangolo di origine o di destinazione cambia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




