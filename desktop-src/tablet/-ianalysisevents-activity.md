---
description: 'Si verifica quando viene chiamato il metodo IInkAnalyzer:: Analyze o IInkAnalyzer:: BackgroundAnalyze.'
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: 'Evento _IAnalysisEvents:: Activity (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351816"
---
# <a name="_ianalysiseventsactivity-event"></a>\_Evento IAnalysisEvents:: Activity

Si verifica quando viene chiamato il metodo [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Activity();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Questo evento indica che [**IInkAnalyzer**](iinkanalyzer.md) sta eseguendo l'analisi dell'input penna. Questo evento non indica lo stato di avanzamento dell'operazione di analisi dell'input penna.

Per eseguire una delle operazioni seguenti, implementare un gestore eventi **\_ IAnalysisEvents:: Activity** :

-   Indica all'utente che l'analizzatore di input penna sta eseguendo l'analisi dell'input penna.
-   Elaborare l'input dell'utente durante l'analisi sincrona.
-   Ricevere una notifica delle richieste di sistema, ad esempio il ridisegno della finestra dell'applicazione, durante l'analisi dell'input penna.

[**IInkAnalyzer**](iinkanalyzer.md) genera spesso questo evento durante la fase di analisi del layout e la fase di classificazione di scrittura e disegno dell'analisi dell'input penna. **IInkAnalyzer** genera questo evento durante la fase di riconoscimento della grafia prima e dopo l'accesso a un riconoscimento input penna.

Il numero di eventi di attività generati da un [**IInkAnalyzer**](iinkanalyzer.md) è influenzato da:

-   Riconoscimento dell'input penna applicato da [**IInkAnalyzer**](iinkanalyzer.md) al riconoscimento dell'input penna.
-   Il numero e la lunghezza dei tratti analizzati da [**IInkAnalyzer**](iinkanalyzer.md) .
-   Numero di tratti classificati come scritti.

Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




