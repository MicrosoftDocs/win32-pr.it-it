---
description: Fornisce l'accesso ai riconoscitori della grafia per l'utilizzo con l'analisi dell'input penna.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Interfaccia IInkAnalysisRecognizer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b091b47d14929e155548dc057ef0fdb1731133a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307405"
---
# <a name="iinkanalysisrecognizer-interface"></a>Interfaccia IInkAnalysisRecognizer

Fornisce l'accesso ai riconoscitori della grafia per l'utilizzo con l'analisi dell'input penna.

## <a name="members"></a>Membri

L'interfaccia **IInkAnalysisRecognizer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalysisRecognizer** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IInkAnalysisRecognizer** dispone di questi metodi.



| Metodo                                                                          | Descrizione                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)               | Recupera le funzionalità del riconoscimento.<br/>                                                                       |
| [**GetGuid**](iinkanalysisrecognizer-getguid.md)                               | Recupera l'identificatore univoco globale (GUID) del riconoscimento.<br/>                                                  |
| [**GetLanguages**](iinkanalysisrecognizer-getlanguages.md)                     | Recupera gli identificatori per le impostazioni locali supportate da questo **IInkAnalysisRecognizer** .<br/>                            |
| [**GetName**](iinkanalysisrecognizer-getname.md)                               | Recupera il nome del riconoscimento.<br/>                                                                               |
| [**GetSupportedProperties**](iinkanalysisrecognizer-getsupportedproperties.md) | Recupera gli identificatori univoci globali (GUID) per le proprietà supportate da questo **IInkAnalysisRecognizer** .<br/> |
| [**Getvendor**](iinkanalysisrecognizer-getvendor.md)                           | Recupera il nome del fornitore del **IInkAnalysisRecognizer**.<br/>                                                        |



 

## <a name="remarks"></a>Commenti

Un riconoscitore ha attributi e proprietà specifici che consentono di eseguire il riconoscimento. È necessario determinare le proprietà di un riconoscimento prima che possa verificarsi il riconoscimento. I tipi di proprietà che un riconoscimento supporta determinano i tipi di riconoscimento che può eseguire. Se, ad esempio, un riconoscimento non supporta la grafia in corsivo, restituisce risultati non accurati quando un utente scrive in corsivo.

Un riconoscimento dispone inoltre di una funzionalità incorporata che gestisce automaticamente molti aspetti della grafia. Ad esempio, determina la metrica per le linee in cui vengono disegnati i tratti. È possibile restituire il numero di riga di un tratto, ma non è mai necessario specificare come vengono determinate le metriche della riga a causa della funzionalità incorporata del riconoscimento.

[**IInkAnalyzer**](iinkanalyzer.md) gestisce un elenco di riconoscitori disponibili. Per accedere a questo elenco, usare il metodo [**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Tipi di nodo di contesto](context-node-types.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

