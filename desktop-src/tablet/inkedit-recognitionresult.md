---
description: Si verifica quando il controllo InkEdit ottiene i risultati manualmente da una chiamata al metodo InkEdit::Recognize o automaticamente dopo l'avvio del timeout di riconoscimento.
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Evento InkEdit.RecognitionResult (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef71d38be31f32c59919a9ce4f24fd90b2d188d86a26e81821f6f7987da31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939081"
---
# <a name="inkeditrecognitionresult-event"></a>InkEdit.RecognitionResult - evento

Si verifica quando [il controllo InkEdit](inkedit-control-reference.md) ottiene i risultati manualmente da una chiamata al metodo [**InkEdit::Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o automaticamente dopo l'avvio del timeout di riconoscimento.

## <a name="syntax"></a>Sintassi


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RecognitionResult* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) che contiene il risultato del riconoscimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito **\_ nell'interfaccia IInkEditEvents.** **\_ L'interfaccia IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore \_ di DISPID IeeRecognitionResult.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inked.h (richiede anche \_ i.c con input penna)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**Controllo \[ InkEdit del metodo Recognize\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)
</dt> </dl>

 

