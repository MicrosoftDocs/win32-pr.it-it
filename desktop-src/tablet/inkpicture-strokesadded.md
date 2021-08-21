---
description: Si verifica quando uno o più oggetti IInkStrokeDisp vengono aggiunti alla raccolta InkStrokes.
ms.assetid: 577ad52b-ecd3-4a49-8997-481ebdb47203
title: Evento InkPicture.StrokesAdded (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5f9418289ac996b2c2248c2cf1696e7d45b4548dbafa4dff9494e76cbedc30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717404"
---
# <a name="inkpicturestrokesadded-event"></a>Evento InkPicture.StrokesAdded

Si verifica quando uno o [**più oggetti IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) vengono aggiunti alla [raccolta InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

## <a name="syntax"></a>Sintassi


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StrokeIds* \[ Pollici\]
</dt> <dd>

Matrice di numeri interi di identificatori per [**ogni oggetto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) aggiunto quando si verifica questo evento.

Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM.](using-the-com-library.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito **\_ nell'interfaccia IInkStrokesEvents.** **\_ L'interfaccia IInkStrokesEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ SEStrokesAdded.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> </dl>

 

