---
description: Carica i risultati dell'analisi salvata in IInkAnalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'Metodo IInkAnalyzer:: LoadResults (IACom. h)'
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
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485076"
---
# <a name="iinkanalyzerloadresults-method"></a>Metodo IInkAnalyzer:: LoadResults

Carica i risultati dell'analisi salvata in [**IInkAnalyzer**](iinkanalyzer.md).

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

*ulDataSize* \[ in\]
</dt> <dd>

Numero di byte in *pbSerializedResults*.

</dd> <dt>

*pbSerializedResults* \[ in\]
</dt> <dd>

Risultati dell'analisi serializzata.

</dd> <dt>

*ulStrokeIdsCount* \[ in\]
</dt> <dd>

Numero degli identificatori del tratto.

</dd> <dt>

*plOriginalStrokeIds* \[ in\]
</dt> <dd>

Matrice di identificatori di tratto originali.

</dd> <dt>

*plNewStrokeIds* \[ in\]
</dt> <dd>

Matrice di nuovi identificatori del tratto.

</dd> <dt>

*pfSuccessful* \[ out, retval\]
</dt> <dd>

**Variante \_ TRUE** se il caricamento è stato eseguito correttamente. in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Quando [**IInkAnalyzer**](iinkanalyzer.md) aggiunge un [**IContextNode**](icontextnode.md) dai risultati salvati, assegna un nuovo identificatore univoco globale (Guid) a **IContextNode** (vedere [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md) e [proprietà del nodo di contesto](context-node-properties.md)).

Questo metodo aggiunge i risultati dell'analisi salvata all'albero [**IContextNode**](icontextnode.md) esistente. Per assicurarsi che i risultati combinati siano ordinati correttamente, aggiungere l'area contenente i nodi di contesto caricati all'area dirty dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) e analizzare nuovamente l'input penna.

I metodi del metodo [**IInkAnalyzer:: SaveResults**](iinkanalyzer-saveresults.md), [**IInkAnalyzer:: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)e [**IInkAnalyzer:: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md) non salvano i dati del pacchetto insieme ai risultati dell'analisi.

Ogni identificatore in *plOriginalStrokeIds* è l'identificatore del tratto per il tratto nei risultati dell'analisi salvata. Ogni identificatore in *plNewStrokeIds* è il nuovo identificatore con cui sostituire l'identificatore originale nei risultati dell'analisi caricata.

Se un hint di analisi salvato è in conflitto con un hint di analisi esistente, [**IInkAnalyzer**](iinkanalyzer.md) non carica l'hint salvato ma carica il resto dei risultati salvati. Tuttavia, se **IInkAnalyzer** carica i risultati per un tratto che si trova all'interno dell'area di un hint di analisi salvato che non viene caricato dal **IInkAnalyzer** , **IInkAnalyzer** aggiunge il rettangolo di delimitazione del tratto all'area dirty dell'oggetto **IInkAnalyzer** . Se, inoltre, **IInkAnalyzer** carica i risultati di un tratto che si trova all'interno di un'area dell'hint di analisi esistente, **IInkAnalyzer** aggiunge anche il rettangolo delimitatore del tratto all'area dirty dell'oggetto **IInkAnalyzer** . Per ulteriori informazioni sugli hint di analisi, vedere [proprietà hint di analisi](analysis-hint-properties.md).

Questo metodo può generare gli eventi [**\_ IAnalysisProxyEvents:: ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ IAnalysisProxyEvents:: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)e [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) durante il caricamento dei risultati salvati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SaveResults**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




