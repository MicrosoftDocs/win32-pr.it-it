---
description: Si verifica quando viene premuto un tasto e nella posizione verso il basso mentre il controllo InkPicture ha lo stato attivo.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: Evento InkPicture.KeyDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9cf86a8efaacd1094330861bff63d38ae03ef056f4686a1286e06c8aca1ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451110"
---
# <a name="inkpicturekeydown-event"></a>Evento InkPicture.KeyDown

Si verifica quando viene premuto un tasto e nella posizione verso il basso mentre il [controllo InkPicture](inkpicture-control-reference.md) ha lo stato attivo.

## <a name="syntax"></a>Sintassi


```C++
void KeyDown(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*KeyCode* \[ in, out\]
</dt> <dd>

Valore ASCII del tasto premuto.

</dd> <dt>

*MAIUSC* \[ in, out\]
</dt> <dd>

Stato del tasto MAIUSC.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito **\_ nell'interfaccia IInkPictureEvents.** **\_ L'interfaccia IInkPictureEvents** implementa [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore \_ DISPID IPEKeyDown.

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

 

