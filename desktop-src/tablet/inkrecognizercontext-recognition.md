---
description: Si verifica quando InkRecognizerContext ha generato risultati dal metodo BackgroundRecognize.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Evento InkRecognizerContext.Recognition (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f6c4799f3366003d14451a19a7bea19ea35aadcce9226f25f1fe80a14ab19e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966940"
---
# <a name="inkrecognizercontextrecognition-event"></a>Evento InkRecognizerContext.Recognition

Si verifica quando [**InkRecognizerContext ha**](inkrecognizercontext-class.md) generato risultati dal [**metodo BackgroundRecognize.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)

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

*RecognizedString* \[ Pollici\]
</dt> <dd>

Testo del risultato del riconoscimento con la massima attendibilità.

Per altre informazioni sul tipo di dati BSTR, vedere [Using the COM Library](using-the-com-library.md).

</dd> <dt>

*CustomData* \[ Pollici\]
</dt> <dd>

Oggetto che contiene i dati personalizzati per il risultato del riconoscimento.

Per altre informazioni sulla struttura VARIANT, vedere [Using the COM Library](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ Pollici\]
</dt> <dd>

Stato di riconoscimento del risultato del riconoscimento più recente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Il comportamento dell'API (Application Programming Interface) è imprevedibile se si tenta di ottenere l'accesso all'oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) originale dal gestore dell'evento di riconoscimento. Non tentare di eseguire questa operazione. Se invece è necessario eseguire questa operazione, creare un flag e impostarlo nel gestore [dell'evento](ink-recognition.md) Recognition. È quindi possibile eseguire il polling del flag per determinare quando modificare le **proprietà InkRecognizerContext** all'esterno del gestore eventi.

Questo metodo di evento è definito \_ nell'interfaccia IInkEvents. \_L'interfaccia IInkEvents implementa [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore \_ di DISPID IRERecognition.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> <dt>

[**Metodo BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[**Enumerazione InkRecognitionStatus**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[**Metodo Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Interfaccia IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

