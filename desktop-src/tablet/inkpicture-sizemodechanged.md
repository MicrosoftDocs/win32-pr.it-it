---
description: Si verifica dopo la modifica della proprietà SizeMode del controllo InkPicture.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: Evento InkPicture. SizeModeChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348656"
---
# <a name="inkpicturesizemodechanged-event"></a>Evento InkPicture. SizeModeChanged

Si verifica dopo la modifica della proprietà [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) del controllo [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Sintassi


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewMode* \[ in\]
</dt> <dd>

Nuovo stato del controllo [InkPicture](inkpicture-control-reference.md) , in base al nuovo valore della proprietà [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .

</dd> <dt>

*OldMode* \[ in\]
</dt> <dd>

Stato precedente del controllo [InkPicture](inkpicture-control-reference.md) , in base al valore precedente della proprietà [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** . L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPESizeModeChanged.

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

 

