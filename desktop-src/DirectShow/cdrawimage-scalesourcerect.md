---
description: Il metodo ScaleSourceRect ridimensiona un rettangolo, se esiste una differenza tra la dimensione del video nativa e il formato del tipo di supporto.
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: Metodo CDrawImage. ScaleSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325327"
---
# <a name="cdrawimagescalesourcerect-method"></a>CDrawImage. ScaleSourceRect, metodo

Il `ScaleSourceRect` metodo ridimensiona un rettangolo, se esiste una differenza tra la dimensione del video nativa e il formato del tipo di supporto.

## <a name="syntax"></a>Sintassi


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSource* 
</dt> <dd>

Puntatore a un rettangolo non ridimensionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il rettangolo ridimensionato.

## <a name="remarks"></a>Commenti

Nella classe **CDrawImage** , questo metodo restituisce *pSource* senza alcuna modifica. È possibile eseguire l'override di questo metodo se il filtro estende l'immagine video in arrivo. Ad esempio, le dimensioni del video nativo potrebbero essere 320 240, ma il tipo di supporto del PIN di input potrebbe essere 640 480. In tal caso, è necessario che il filtro Ridimensiona il rettangolo di origine in base a un fattore di 2.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




