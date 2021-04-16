---
description: In questa sezione vengono fornite informazioni sulle interfacce e sulle classi utilizzate nell'analisi degli input penna. Le classi e le interfacce dell'analisi dell'input penna non sono conformi all'automazione.
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: Interfacce e classi di analisi dell'input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1c157a08a4b7366c20a712c120265320ab4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524936"
---
# <a name="ink-analysis-classes-and-interfaces"></a>Interfacce e classi di analisi dell'input penna

In questa sezione vengono fornite informazioni sulle interfacce e sulle classi utilizzate nell'analisi degli input penna. Le classi e le interfacce dell'analisi dell'input penna non sono conformi all'automazione.

## <a name="classes"></a>Classi



| Classe                                    | Descrizione                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [**AnalysisRegion**](analysisregion.md) | Implementa l'interfaccia [**IAnalysisRegion**](ianalysisregion.md) .<br/> |
| [**InkAnalyzer**](inkanalyzer.md)       | Implementa l'interfaccia [**IInkAnalyzer**](iinkanalyzer.md) .<br/>       |



 

## <a name="interfaces"></a>Interfacce



| Interfaccia                                                    | Descrizione                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAnalysisAlternate**](ianalysisalternate.md)             | Rappresenta le possibili corrispondenze delle parole per il riconoscimento della grafia per gli oggetti [**IContextNode**](icontextnode.md) .<br/>                                                                                        |
| [**IAnalysisAlternates**](ianalysisalternates.md)           | Contiene una raccolta di oggetti che implementano l'interfaccia [**IAnalysisAlternate**](ianalysisalternate.md) e che sono il risultato dell'analisi dell'input penna.<br/>                                               |
| [**IAnalysisRegion**](ianalysisregion.md)                   | Espone metodi e proprietà per un'area che rappresenta un'area di un documento.<br/>                                                                                                                    |
| [**IAnalysisStatus**](ianalysisstatus.md)                   | Rappresenta lo stato dell'operazione di analisi dell'input penna indicando se l'analisi è stata completata correttamente e se sono stati generati avvisi.<br/>                                                  |
| [**IAnalysisWarning**](ianalysiswarning.md)                 | Rappresenta un avviso o un errore che si verifica durante un'operazione di analisi dell'input penna.<br/>                                                                                                                           |
| [**IAnalysisWarnings**](ianalysiswarnings.md)               | Contiene una raccolta di oggetti che implementano l'interfaccia [**IAnalysisWarning**](ianalysiswarning.md) e che sono il risultato di un'operazione di analisi dell'input penna.<br/>                                      |
| [**IContextLink**](icontextlink.md)                         | Rappresenta una relazione tra due oggetti [**IContextNode**](icontextnode.md) .<br/>                                                                                                                   |
| [**IContextLinks**](icontextlinks.md)                       | Contiene una raccolta di oggetti che implementano l'interfaccia [**IContextLink**](icontextlink.md) .<br/>                                                                                                   |
| [**IContextNode**](icontextnode.md)                         | Rappresenta un nodo in un albero di oggetti creati come parte dell'analisi dell'input penna.<br/>                                                                                                                      |
| [**IContextNodes**](icontextnodes.md)                       | Contiene una raccolta di oggetti che implementano l'interfaccia [**IContextNode**](icontextnode.md) e che sono il risultato di un'operazione di analisi dell'input penna.<br/>                                              |
| [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)     | Fornisce l'accesso ai riconoscitori della grafia per l'utilizzo con l'analisi dell'input penna.<br/>                                                                                                                                 |
| [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)   | Contiene una raccolta di oggetti che implementano l'interfaccia [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) e che rappresentano la possibilità di riconoscere grafia, oggetti o movimenti.<br/> |
| [**IInkAnalyzer**](iinkanalyzer.md)                         | Consente di accedere all'analisi del layout, alla classificazione di scrittura e disegno e al riconoscimento della grafia.<br/>                                                                                                  |
| [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) | Espone un metodo per valutare se un oggetto [**IContextNode**](icontextnode.md) soddisfa o meno un criterio specificato.<br/>                                                                              |



 

## <a name="return-values"></a>Valori restituiti

I metodi della libreria COM di Tablet PC restituiscono valori **HRESULT**. Se non specificato diversamente, in questa tabella vengono descritti i significati dei valori **HRESULT** .



| Valore HRESULT                                   | Descrizione                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| \_OK<br/>                                | Esito positivo.<br/>                                                                      |
| \_puntatore E<br/>                           | Almeno un puntatore (per un parametro di input o di output) non è valido.<br/> |
| E \_ INVALIDARG<br/>                        | Il membro ha tentato di passare un argomento non valido.<br/>                              |
| E \_ \_ eccezione Ink<br/>                    | Si è verificata un'eccezione.<br/>                                                           |
| E \_ OutOfMemory<br/>                       | Il sistema non è in grado di allocare memoria per completare l'operazione.<br/>                      |
| E \_ non riescono<br/>                              | Si è verificato un errore non specificato.<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | Il membro ha tentato di usare un'operazione non valida.<br/>                                 |
| \_modalità TPC E \_ non valida \_<br/>                | Il membro ha tentato di usare una modalità non valida.<br/>                                      |
| \_configurazione TPC E \_ non valida \_<br/>       | Il membro ha tentato di usare una configurazione non valida.<br/>                             |
| \_Descrizione pacchetto TPC E \_ non valida \_ \_<br/> | Il membro ha tentato di usare una descrizione del pacchetto non valida.<br/>                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




