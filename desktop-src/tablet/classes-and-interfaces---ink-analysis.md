---
description: Questa sezione contiene informazioni sulle interfacce e sulle classi usate nell'analisi dell'input penna. Le classi e le interfacce di analisi dell'input penna non sono conformi all'automazione.
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: Classi e interfacce di analisi dell'input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48335b0e7bf6e29ee90cf1dbf8fb3e96fd761c4b8c0194daaa9d7365fe89d5c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937021"
---
# <a name="ink-analysis-classes-and-interfaces"></a>Classi e interfacce di analisi dell'input penna

Questa sezione contiene informazioni sulle interfacce e sulle classi usate nell'analisi dell'input penna. Le classi e le interfacce di analisi dell'input penna non sono conformi all'automazione.

## <a name="classes"></a>Classi



| Classe                                    | Descrizione                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [**Analysisregion**](analysisregion.md) | Implementa [**l'interfaccia IAnalysisRegion.**](ianalysisregion.md)<br/> |
| [**Inkanalyzer**](inkanalyzer.md)       | Implementa [**l'interfaccia IInkAnalyzer.**](iinkanalyzer.md)<br/>       |



 

## <a name="interfaces"></a>Interfacce



| Interfaccia                                                    | Descrizione                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAnalysisAlternate**](ianalysisalternate.md)             | Rappresenta le possibili corrispondenze di parole di riconoscimento della grafia per [**gli oggetti IContextNode.**](icontextnode.md)<br/>                                                                                        |
| [**IAnalysisAlternates**](ianalysisalternates.md)           | Contiene una raccolta di oggetti che implementano [**l'interfaccia IAnalysisAlternate**](ianalysisalternate.md) e che sono il risultato dell'analisi dell'input penna.<br/>                                               |
| [**Area IAnalysis**](ianalysisregion.md)                   | Espone metodi e proprietà per un'area che rappresenta un'area di un documento.<br/>                                                                                                                    |
| [**IAnalysisStatus**](ianalysisstatus.md)                   | Rappresenta lo stato dell'operazione di analisi input penna descrivendo se l'analisi è stata completata correttamente e se si sono verificati avvisi.<br/>                                                  |
| [**IAnalysisWarning**](ianalysiswarning.md)                 | Rappresenta un avviso o un errore che si verifica durante un'operazione di analisi dell'input penna.<br/>                                                                                                                           |
| [**IAnalysisWarnings**](ianalysiswarnings.md)               | Contiene una raccolta di oggetti che implementano [**l'interfaccia IAnalysisWarning**](ianalysiswarning.md) e che sono il risultato di un'operazione di analisi dell'input penna.<br/>                                      |
| [**IContextLink**](icontextlink.md)                         | Rappresenta una relazione tra due [**oggetti IContextNode.**](icontextnode.md)<br/>                                                                                                                   |
| [**IContextLinks**](icontextlinks.md)                       | Contiene una raccolta di oggetti che implementano [**l'interfaccia IContextLink.**](icontextlink.md)<br/>                                                                                                   |
| [**IContextNode**](icontextnode.md)                         | Rappresenta un nodo in un albero di oggetti creati come parte dell'analisi dell'input penna.<br/>                                                                                                                      |
| [**IContextNodes**](icontextnodes.md)                       | Contiene una raccolta di oggetti che implementano [**l'interfaccia IContextNode**](icontextnode.md) e che sono il risultato di un'operazione di analisi dell'input penna.<br/>                                              |
| [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)     | Fornisce l'accesso ai riconoscitori della grafia da usare con l'analisi dell'input penna.<br/>                                                                                                                                 |
| [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)   | Contiene una raccolta di oggetti che implementano [**l'interfaccia IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) e che rappresentano la possibilità di riconoscere la grafia, gli oggetti o i movimenti.<br/> |
| [**IInkAnalyzer**](iinkanalyzer.md)                         | Consente di accedere all'analisi del layout, alla classificazione di scrittura e disegno e al riconoscimento della grafia.<br/>                                                                                                  |
| [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) | Espone un metodo per valutare se un [**oggetto IContextNode**](icontextnode.md) soddisfa o meno un criterio specificato.<br/>                                                                              |



 

## <a name="return-values"></a>Valori restituiti

I metodi nella libreria COM di Tablet PC restituiscono valori **HRESULT**. Se non diversamente specificato, i significati dei **valori HRESULT** sono descritti in questa tabella.



| Valore HRESULT                                   | Descrizione                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ OK<br/>                                | Operazione completata.<br/>                                                                      |
| PUNTATORE E \_<br/>                           | Almeno un puntatore (per un input o un parametro di output) non è valido.<br/> |
| E \_ INVALIDARG<br/>                        | Il membro ha tentato di passare un argomento non valido.<br/>                              |
| E \_ ECCEZIONE \_ DELL'INPUT PENNA<br/>                    | Si è verificata un'eccezione.<br/>                                                           |
| E \_ OUTOFMEMORY<br/>                       | Impossibile allocare memoria per completare l'operazione.<br/>                      |
| E \_ FAIL<br/>                              | Si è verificato un errore non specificato.<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | Il membro ha tentato di usare un'operazione non valida.<br/>                                 |
| MODALITÀ TPC \_ E \_ NON \_ VALIDA<br/>                | Il membro ha tentato di usare una modalità non valida.<br/>                                      |
| CONFIGURAZIONE TPC \_ E \_ NON \_ VALIDA<br/>       | Il membro ha tentato di usare una configurazione non valida.<br/>                             |
| DESCRIZIONE \_ DEL PACCHETTO TPC E NON \_ \_ \_ VALIDA<br/> | Il membro ha tentato di usare una descrizione del pacchetto non valida.<br/>                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




