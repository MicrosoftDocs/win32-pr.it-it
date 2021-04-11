---
description: Rappresenta le possibili corrispondenze delle parole per il riconoscimento della grafia per gli oggetti IContextNode.
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: Interfaccia IAnalysisAlternate (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226177"
---
# <a name="ianalysisalternate-interface"></a>Interfaccia IAnalysisAlternate

Rappresenta le possibili corrispondenze delle parole per il riconoscimento della grafia per gli oggetti [**IContextNode**](icontextnode.md) .

## <a name="members"></a>Membri

L'interfaccia **IAnalysisAlternate** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisAlternate** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAnalysisAlternate** dispone di questi metodi.



| Metodo                                                                          | Descrizione                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAlternateNodes**](ianalysisalternate-getalternatenodes.md)               | Recupera gli oggetti [**IContextNode**](icontextnode.md) associati a questa alternativa.<br/>                                                       |
| [**GetRecognitionConfidence**](ianalysisalternate-getrecognitionconfidence.md) | Recupera un valore che indica il livello di attendibilità di [**IInkAnalyzer**](iinkanalyzer.md) nell'accuratezza di **IAnalysisAlternate**.<br/> |
| [**GetRecognizedString**](ianalysisalternate-getrecognizedstring.md)           | Recupera il valore stringa riconosciuto dell'oggetto **IAnalysisAlternate** .<br/>                                                                               |
| [**GetStrokeIds**](ianalysisalternate-getstrokeids.md)                         | Recupera gli identificatori di tratto associati a questo **IAnalysisAlternate**.<br/>                                                                    |



 

## <a name="remarks"></a>Commenti

Esistono molte varianti nella grafia degli utenti. Per questo motivo, i riconoscitori della grafia possono a volte convertire la grafia in testo diverso da quello previsto dall'utente. Quando un [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi su una raccolta di tratti, il **IInkAnalyzer** trova il set di parole più probabile rappresentato dalla grafia. Inoltre, **IInkAnalyzer** trova anche set di corrispondenze di riconoscimento alternative, che vengono archiviate in una raccolta [**IAnalysisAlternates**](ianalysisalternates.md) . Per consentire a un utente di sfruttare le alternative di riconoscimento, è necessario creare un'interfaccia utente che consenta all'utente di selezionare il **IAnalysisAlternate** corretto.

Gli oggetti **IAnalysisAlternate** vengono in genere ottenuti tramite il [**Metodo IInkAnalyzer:: GetAlternates**](iinkanalyzer-getalternates.md). Il primo oggetto **IAnalysisAlternate** nella raccolta è quello che [**IInkAnalyzer**](iinkanalyzer.md) considera l'alternativa più probabile.

Questa interfaccia è equivalente a [System. Windows. Ink. AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) nel .NET Framework.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: getalters**](iinkanalyzer-getalternates.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

