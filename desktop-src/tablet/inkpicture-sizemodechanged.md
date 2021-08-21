---
description: Si verifica dopo la modifica della proprietà SizeMode del controllo InkPicture.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: Evento InkPicture.SizeModeChanged (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebcd5a659894c6f70a87ea75f7a99321d94dba2826fd538530f7e6d060d5730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032029"
---
# <a name="inkpicturesizemodechanged-event"></a>Evento InkPicture.SizeModeChanged

Si verifica dopo la modifica della proprietà [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) del [controllo InkPicture.](inkpicture-control-reference.md)

## <a name="syntax"></a>Sintassi


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewMode* \[ Pollici\]
</dt> <dd>

Nuovo stato del [controllo InkPicture,](inkpicture-control-reference.md) in base al nuovo valore della [**proprietà SizeMode.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)

</dd> <dt>

*OldMode* \[ Pollici\]
</dt> <dd>

Stato precedente del [controllo InkPicture,](inkpicture-control-reference.md) in base al valore precedente della [**proprietà SizeMode.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito **\_ nell'interfaccia IInkPictureEvents.** **\_ L'interfaccia IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore \_ DISPID IPESizeModeChanged.

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

 

