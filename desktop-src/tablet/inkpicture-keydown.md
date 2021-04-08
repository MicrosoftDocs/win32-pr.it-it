---
description: Si verifica quando viene premuto un tasto e nella posizione in giù mentre il controllo InkPicture dispone dello stato attivo.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: Evento InkPicture. KeyDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5d6bd3555aeec98ac28555c1674dfef32ecc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058334"
---
# <a name="inkpicturekeydown-event"></a>Evento InkPicture. KeyDown

Si verifica quando viene premuto un tasto e nella posizione in giù mentre il controllo [InkPicture](inkpicture-control-reference.md) dispone dello stato attivo.

## <a name="syntax"></a>Sintassi


```C++
void KeyDown(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Codice* \[ di stato in uscita\]
</dt> <dd>

Valore ASCII della chiave da premere.

</dd> <dt>

*Sposta* \[ in uscita\]
</dt> <dd>

Stato del tasto MAIUSC.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** . L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPEKeyDown.

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

 

