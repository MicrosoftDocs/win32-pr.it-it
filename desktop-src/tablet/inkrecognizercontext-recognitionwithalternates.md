---
description: Si verifica quando la classe InkRecognizerContext genera risultati dopo la chiamata al metodo del metodo BackgroundRecognizeWithAlternates.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Evento InkRecognizerContext. RecognitionWithAlternates (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232483"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a>Evento InkRecognizerContext. RecognitionWithAlternates

Si verifica quando la [**classe InkRecognizerContext**](inkrecognizercontext-class.md) genera risultati dopo la chiamata al metodo del [**metodo BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) .

## <a name="syntax"></a>Sintassi


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RecognitionResult* \[ in\]
</dt> <dd>

Risultato del riconoscimento dall'evento.

</dd> <dt>

*CustomData* \[ in\]
</dt> <dd>

Dati personalizzati per il risultato del riconoscimento.

Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ in\]
</dt> <dd>

Stato di riconoscimento del risultato del riconoscimento più recente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il comportamento del Application Programming Interface (API) è imprevedibile se si tenta di ottenere l'accesso all'oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) originale dal gestore dell'evento di riconoscimento. Non tentare di eseguire questa operazione. In alternativa, se è necessario eseguire questa operazione, creare un flag e impostarlo nel gestore dell'evento di [**riconoscimento**](inkrecognizercontext-recognition.md) . È quindi possibile eseguire il polling del flag per determinare quando modificare le proprietà **InkRecognizerContext** all'esterno del gestore eventi.

Questo metodo di evento è definito nell' \_ interfaccia IInkEvents. L' \_ interfaccia IInkEvents implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IRERecognitionWithAlternates.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> <dt>

[**Metodo BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[**Recognize (metodo)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Interfaccia IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

