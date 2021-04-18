---
description: Si verifica quando InkRecognizerContext ha generato risultati dal metodo BackgroundRecognize.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Evento InkRecognizerContext. Recognition (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316831"
---
# <a name="inkrecognizercontextrecognition-event"></a>Evento InkRecognizerContext. Recognition

Si verifica quando [**InkRecognizerContext**](inkrecognizercontext-class.md) ha generato risultati dal metodo [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) .

## <a name="syntax"></a>Sintassi


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RecognizedString* \[ in\]
</dt> <dd>

Testo del risultato del riconoscimento con la massima confidenza.

Per ulteriori informazioni sul tipo di dati BSTR, vedere [utilizzando la libreria com](using-the-com-library.md).

</dd> <dt>

*CustomData* \[ in\]
</dt> <dd>

Oggetto che contiene i dati personalizzati per il risultato del riconoscimento.

Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzando la libreria com](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ in\]
</dt> <dd>

Stato di riconoscimento del risultato del riconoscimento più recente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il comportamento del Application Programming Interface (API) è imprevedibile se si tenta di ottenere l'accesso all'oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) originale dal gestore dell'evento di riconoscimento. Non tentare di eseguire questa operazione. In alternativa, se è necessario eseguire questa operazione, creare un flag e impostarlo nel gestore dell'evento di [riconoscimento](ink-recognition.md) . È quindi possibile eseguire il polling del flag per determinare quando modificare le proprietà **InkRecognizerContext** all'esterno del gestore eventi.

Questo metodo di evento è definito nell' \_ interfaccia IInkEvents. L' \_ interfaccia IInkEvents implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IRERecognition.

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

[**Metodo BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[**Enumerazione InkRecognitionStatus**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[**Recognize (metodo)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Interfaccia IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

