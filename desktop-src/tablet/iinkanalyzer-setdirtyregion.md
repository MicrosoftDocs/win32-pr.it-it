---
description: Modifica l'area modificata dopo l'ultima operazione di analisi.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: Metodo IInkAnalyzer::SetDirtyRegion (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a39fc420b368911788efcb9462c9c4be5b4828c82906ef2c94bb5be99ca17568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091471"
---
# <a name="iinkanalyzersetdirtyregion-method"></a>Metodo IInkAnalyzer::SetDirtyRegion

Modifica l'area modificata dopo l'ultima operazione di analisi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDirtyRegion* \[ Pollici\]
</dt> <dd>

[**IAnalysisRegion che**](ianalysisregion.md) descrive l'area modificata dopo l'ultima operazione di analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Questo metodo identifica le aree che devono essere analizzate o analizzate di nuovo. Tutti i metodi [**IInkAnalyzer**](iinkanalyzer.md) che aggiungono, aggiornano o rimuovono i dati dei tratti aggiornano l'area dirty. Per contrassegnare manualmente un'area per la rianalisi:

1.  Ottenere l'area dirty [**usando il metodo IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md).
2.  Usare [**il metodo IAnalysisRegion::UnionRegion**](ianalysisregion-unionregion.md) o il metodo [**IAnalysisRegion::UnionRectangle**](ianalysisregion-unionrectangle.md) per aggiungere l'area all'area del passaggio 1.
3.  Usare **il metodo IInkAnalyzer::SetDirtyRegion** per aggiornare l'area dirty.

[**IInkAnalyzer**](iinkanalyzer.md) analizza l'input penna all'interno della relativa area dirty durante una chiamata al metodo [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) o al metodo [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md). Tuttavia, **IInkAnalyzer può** espandere l'operazione di analisi per includere le aree adiacenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer::RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




