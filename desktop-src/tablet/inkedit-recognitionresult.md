---
description: "Si verifica quando il controllo InkEdit ottiene manualmente i risultati da una chiamata al Metodo InkEdit:: Recognize o automaticamente dopo l'attivazione del timeout di riconoscimento."
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Evento InkEdit. RecognitionResult (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233557"
---
# <a name="inkeditrecognitionresult-event"></a>Evento InkEdit. RecognitionResult

Si verifica quando il controllo [InkEdit](inkedit-control-reference.md) ottiene manualmente i risultati da una chiamata al metodo [**InkEdit:: Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o automaticamente dopo l'attivazione del timeout di riconoscimento.

## <a name="syntax"></a>Sintassi


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RecognitionResult* \[ in\]
</dt> <dd>

Oggetto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) che contiene il risultato del riconoscimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** . L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeRecognitionResult.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inchiostrato. h (richiede anche il \_ . c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Metodo Recognize ( \[ controllo InkEdit)\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)
</dt> </dl>

 

