---
description: Il metodo GetPaletteVersion recupera la versione corrente della tavolozza.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: Metodo CDrawImage.GetPaletteVersion (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14cc4df95507a0c28bd61ec6db405f01353f9228419d0da84c4fc9fc35ca6b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537291"
---
# <a name="cdrawimagegetpaletteversion-method"></a>Metodo CDrawImage.GetPaletteVersion

Il `GetPaletteVersion` metodo recupera la versione corrente della tavolozza.

## <a name="syntax"></a>Sintassi


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore della variabile **\_ membro m PaletteVersion.**

## <a name="remarks"></a>Commenti

Il valore restituito da questo metodo si applica solo quando l'allocatore è un [**oggetto CImageAllocator.**](cimageallocator.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[**CDrawImage::ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




