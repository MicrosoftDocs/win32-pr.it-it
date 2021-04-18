---
description: Il metodo SetStretchMode calcola se l'immagine video deve essere allungata.
ms.assetid: ffdcaf9c-e157-4557-9193-8430c1c451bf
title: Metodo CDrawImage. SetStretchMode (Winutil. h)
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
ms.openlocfilehash: 33a4b3a6b104b9e2888776cc59183835f412fdcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333720"
---
# <a name="cdrawimagesetstretchmode-method"></a>CDrawImage. SetStretchMode, metodo

Il `SetStretchMode` metodo calcola se l'immagine video deve essere allungata.

## <a name="syntax"></a>Sintassi


```C++
void SetStretchMode();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La classe **CDrawImage** chiama automaticamente questo metodo ogni volta che viene modificato il rettangolo di origine o di destinazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




