---
description: Il metodo IncrementPaletteVersion incrementa la versione della tavolozza. Chiamare questo metodo se il tipo di supporto viene modificato in un nuovo formato non formattato.
ms.assetid: 1ce77f97-d225-45f5-a259-1dcca1272d15
title: Metodo CDrawImage.IncrementPaletteVersion (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.IncrementPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7884c4d552920a9e5650d2a092b7fffc43a1c67bf03916eab7bb72da3a87946a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076401"
---
# <a name="cdrawimageincrementpaletteversion-method"></a>Metodo CDrawImage.IncrementPaletteVersion

Il `IncrementPaletteVersion` metodo incrementa la versione della tavolozza. Chiamare questo metodo se il tipo di supporto viene modificato in un nuovo formato non formattato.

## <a name="syntax"></a>Sintassi


```C++
void IncrementPaletteVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo incrementa il valore della variabile **membro m \_ PaletteVersion.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::GetPaletteVersion**](cdrawimage-getpaletteversion.md)
</dt> <dt>

[**CDrawImage::ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




