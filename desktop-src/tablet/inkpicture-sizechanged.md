---
description: Si verifica dopo che il controllo InkPicture è stato ridimensionato, in particolare, dopo la modifica del valore della proprietà Width o Height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Evento InkPicture. SizeChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968420"
---
# <a name="inkpicturesizechanged-event"></a>Evento InkPicture. SizeChanged

Si verifica dopo che il controllo [InkPicture](inkpicture-control-reference.md) è stato ridimensionato, in particolare, dopo la modifica del valore della proprietà [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) o [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .

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

A *sinistra* \[ in\]
</dt> <dd>

Coordinata x del lato sinistro del controllo [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

In *alto* \[ in\]
</dt> <dd>

Coordinata y della parte superiore del controllo [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

A *destra* \[ in\]
</dt> <dd>

Coordinata x del lato destro del controllo [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

In *basso* \[ in\]
</dt> <dd>

Coordinata y della parte inferiore del controllo [InkPicture](inkpicture-control-reference.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** . L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPESizeChanged.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

