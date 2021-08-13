---
description: Fornisce l'accesso ai riconoscitori della grafia da usare con l'analisi dell'input penna.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Interfaccia IInkAnalysisRecognizer (IACom.h)
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
ms.openlocfilehash: d0736288658c57c1cfd346b8337f91353638b8326ed1d0b29687c812db72efba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350881"
---
# <a name="iinkanalysisrecognizer-interface"></a>Interfaccia IInkAnalysisRecognizer

Fornisce l'accesso ai riconoscitori della grafia da usare con l'analisi dell'input penna.

## <a name="members"></a>Membri

**L'interfaccia IInkAnalysisRecognizer** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IInkAnalysisRecognizer** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IInkAnalysisRecognizer.**



| Metodo                                                                          | Descrizione                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)               | Recupera le funzionalità del riconoscimento.<br/>                                                                       |
| [**GetGuid**](iinkanalysisrecognizer-getguid.md)                               | Recupera l'identificatore univoco globale (GUID) del riconoscimento.<br/>                                                  |
| [**GetLanguages**](iinkanalysisrecognizer-getlanguages.md)                     | Recupera gli identificatori per le impostazioni locali supportate da **IInkAnalysisRecognizer.**<br/>                            |
| [**GetName**](iinkanalysisrecognizer-getname.md)                               | Recupera il nome del riconoscitore.<br/>                                                                               |
| [**GetSupportedProperties**](iinkanalysisrecognizer-getsupportedproperties.md) | Recupera gli identificatori univoci globali (GUID) per le proprietà supportate da **IInkAnalysisRecognizer.**<br/> |
| [**GetVendor**](iinkanalysisrecognizer-getvendor.md)                           | Recupera il nome del fornitore di **IInkAnalysisRecognizer.**<br/>                                                        |



 

## <a name="remarks"></a>Commenti

Un riconoscitore ha attributi e proprietà specifici che gli consentono di eseguire il riconoscimento. Le proprietà di un riconoscitore devono essere determinate prima che possa verificarsi il riconoscimento. I tipi di proprietà supportati da un sistema di riconoscimento determinano i tipi di riconoscimento che può eseguire. Se, ad esempio, un sistema di riconoscimento non supporta la scrittura con scrittura in scrittura incurva, restituisce risultati non accurati quando un utente scrive in modo curvo.

Un sistema di riconoscimento include anche funzionalità incorporate che gestiscono automaticamente molti aspetti della scrittura manuale. Ad esempio, determina le metriche per le linee su cui vengono disegnati i tratti. È possibile restituire il numero di riga di un tratto, ma non è mai necessario specificare come vengono determinate le metriche della linea a causa della funzionalità predefinita del riconoscimento.

[**IInkAnalyzer**](iinkanalyzer.md) gestisce un elenco di riconoscitori disponibili. Per accedere a questo elenco, usare il metodo [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority.**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Tipi di nodo di contesto](context-node-types.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

