---
description: Contiene una raccolta di oggetti che implementano l'interfaccia IInkAnalysisRecognizer e che rappresentano la possibilità di riconoscere grafia, oggetti o movimenti.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Interfaccia IInkAnalysisRecognizers (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343716"
---
# <a name="iinkanalysisrecognizers-interface"></a>Interfaccia IInkAnalysisRecognizers

Contiene una raccolta di oggetti che implementano l'interfaccia [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) e che rappresentano la possibilità di riconoscere grafia, oggetti o movimenti.

## <a name="members"></a>Membri

L'interfaccia **IInkAnalysisRecognizers** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalysisRecognizers** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IInkAnalysisRecognizers** dispone di questi metodi.



| Metodo                                                                               | Descrizione                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iinkanalysisrecognizers-getcount.md)                                 | Recupera il numero di oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) in questa raccolta.<br/> |
| [**GetInkAnalysisRecognizer**](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | Recupera l'oggetto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) in corrispondenza dell'indice specificato.<br/>               |



 

## <a name="remarks"></a>Commenti

Il metodo [**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) metodo di [**IInkAnalyzer**](iinkanalyzer.md) restituisce una raccolta **IInkAnalysisRecognizers** contenente i riconoscitori Ink disponibili sul Tablet PC corrente.

Per un riconoscimento della lingua, il metodo [**IInkAnalysisRecognizer:: GetLanguages**](iinkanalysisrecognizer-getlanguages.md) restituisce una matrice non vuota. Per i riconoscitori di movimento e i riconoscitori di oggetti, il metodo **IInkAnalysisRecognizer:: GetLanguages** restituisce una matrice vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

