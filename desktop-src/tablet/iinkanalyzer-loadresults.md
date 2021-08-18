---
description: Carica i risultati dell'analisi salvati in IInkAnalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: Metodo IInkAnalyzer::LoadResults (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 47f385334f1b16f3d7de46b8cfc53ee6b94f485c9768f973b745af335cd5c12f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713381"
---
# <a name="iinkanalyzerloadresults-method"></a>Metodo IInkAnalyzer::LoadResults

Carica i risultati dell'analisi salvati in [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulDataSize* \[ Pollici\]
</dt> <dd>

Numero di byte in *pbSerializedResults.*

</dd> <dt>

*pbSerializedResults* \[ Pollici\]
</dt> <dd>

Risultati dell'analisi serializzata.

</dd> <dt>

*ulStrokeIdsCount* \[ Pollici\]
</dt> <dd>

Numero di identificatori di tratti.

</dd> <dt>

*plOriginalStrokeIds* \[ Pollici\]
</dt> <dd>

Matrice di identificatori di tratti originali.

</dd> <dt>

*plNewStrokeIds* \[ Pollici\]
</dt> <dd>

Matrice di nuovi identificatori di tratto.

</dd> <dt>

*pfSuccessful* \[ out, retval\]
</dt> <dd>

**VARIANT \_ TRUE se** il caricamento ha avuto esito positivo; in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Quando [**IInkAnalyzer**](iinkanalyzer.md) aggiunge un [**oggetto IContextNode**](icontextnode.md) dai risultati salvati, assegna un nuovo identificatore univoco globale (GUID) a **IContextNode** (vedere [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md) e proprietà del nodo [di](context-node-properties.md)contesto).

Questo metodo aggiunge i risultati dell'analisi salvata all'albero [**IContextNode**](icontextnode.md) esistente. Per assicurarsi che i risultati combinati siano ordinati correttamente, aggiungere l'area contenente i nodi di contesto caricati all'area dirty dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere Il metodo [**IInkAnalyzer::GetDirtyRegion)**](iinkanalyzer-getdirtyregion.md)e rianalyizzare l'input penna.

I metodi [**IInkAnalyzer::SaveResults,**](iinkanalyzer-saveresults.md) [**IInkAnalyzer::SaveResultsForNodes e**](iinkanalyzer-saveresultsfornodes.md) [**IInkAnalyzer::SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md) non salvano i dati del pacchetto insieme ai risultati dell'analisi.

Ogni identificatore in *plOriginalStrokeIds* è l'identificatore del tratto nei risultati dell'analisi salvati. Ogni identificatore in *plNewStrokeIds* è il nuovo identificatore con cui sostituire l'identificatore originale nei risultati dell'analisi caricata.

Se un hint di analisi salvato è in conflitto con un hint di analisi esistente, [**IInkAnalyzer**](iinkanalyzer.md) non carica l'hint salvato, ma carica il resto dei risultati salvati. Tuttavia, se **IInkAnalyzer** carica i risultati per un tratto che si trova all'interno dell'area di un suggerimento di analisi salvato che **IInkAnalyzer** non viene caricato, **IInkAnalyzer** aggiunge il rettangolo di selezione del tratto all'area dirty dell'oggetto **IInkAnalyzer.** Inoltre, se **IInkAnalyzer** carica i risultati per un tratto che si trova all'interno dell'area di un hint di analisi esistente, **L'oggetto IInkAnalyzer** aggiunge anche il rettangolo di selezione del tratto all'area dirty dell'oggetto **IInkAnalyzer.** Per altre informazioni sugli hint di analisi, vedere [Proprietà hint di analisi](analysis-hint-properties.md).

Questo metodo può generare gli eventi [**\_ IAnalysisProxyEvents::ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)e [**\_ IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) durante il caricamento dei risultati salvati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SaveResults**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




