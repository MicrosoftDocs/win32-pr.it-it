---
description: Il metodo ResetPaletteVersion reimposta la versione della tavolozza. Chiamare questo metodo se il pin del filtro proprietario si riconnette.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: Metodo CDrawImage.ResetPaletteVersion (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d367060c86c54fb9df5bd7b0f05cea1fa3d7b7f3316dce327fca7ce9985fadfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055961"
---
# <a name="cdrawimageresetpaletteversion-method"></a>Metodo CDrawImage.ResetPaletteVersion

Il `ResetPaletteVersion` metodo reimposta la versione della tavolozza. Chiamare questo metodo se il pin del filtro proprietario si riconnette.

## <a name="syntax"></a>Sintassi


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo imposta il valore di **m \_ PaletteVersion** su una costante predefinita, **PALETTE \_ VERSION.**

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

[**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




