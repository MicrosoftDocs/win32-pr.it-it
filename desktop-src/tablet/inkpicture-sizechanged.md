---
description: Si verifica dopo il ridimensionamento del controllo InkPicture, in particolare dopo la modifica del valore della proprietà Width o Height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Evento InkPicture.SizeChanged (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4473bf580e1683c8d410cd1f2cdbaf271302485f51556b68c4fae7a5d6b99ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032039"
---
# <a name="inkpicturesizechanged-event"></a>Evento InkPicture.SizeChanged

Si verifica dopo il ridimensionamento del controllo [InkPicture,](inkpicture-control-reference.md) in particolare dopo la modifica del valore della proprietà [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) o [**Height.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)

## <a name="syntax"></a>Sintassi


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*A sinistra* \[ Pollici\]
</dt> <dd>

Coordinata x del lato sinistro del [controllo InkPicture.](inkpicture-control-reference.md)

</dd> <dt>

*In alto* \[ Pollici\]
</dt> <dd>

Coordinata y della parte superiore del [controllo InkPicture.](inkpicture-control-reference.md)

</dd> <dt>

*A destra* \[ Pollici\]
</dt> <dd>

Coordinata x del lato destro del [controllo InkPicture.](inkpicture-control-reference.md)

</dd> <dt>

*In basso* \[ Pollici\]
</dt> <dd>

Coordinata y della parte inferiore del [controllo InkPicture.](inkpicture-control-reference.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito **\_ nell'interfaccia IInkPictureEvents.** **\_ L'interfaccia IInkPictureEvents** implementa [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore \_ DISPID IPESizeChanged.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> </dl>

 

