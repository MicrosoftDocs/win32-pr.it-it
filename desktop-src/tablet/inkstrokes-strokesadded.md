---
description: Si verifica quando uno o più tratti vengono aggiunti alla raccolta InkStrokes.
ms.assetid: d32dcaef-3beb-4ee1-84d6-5944278936f6
title: Evento InkStrokes. StrokesAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a53bf1f511b5809cfb9a6ca0a2f683f0e85540af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313924"
---
# <a name="inkstrokesstrokesadded-event"></a>Evento InkStrokes. StrokesAdded

Si verifica quando uno o più tratti vengono aggiunti alla raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

## <a name="syntax"></a>Sintassi


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StrokeIds* \[ in\]
</dt> <dd>

Matrice di interi degli identificatori per ogni oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) aggiunto quando si verifica questo evento.

Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nell' \_ interfaccia IInkEvents. L' \_ interfaccia IInkEvents implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ SEStrokesAdded.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Aggiungi metodo \[ InkStrokes collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)
</dt> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> </dl>

 

