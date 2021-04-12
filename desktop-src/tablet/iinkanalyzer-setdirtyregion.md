---
description: Modifica l'area che è stata modificata dopo l'ultima operazione di analisi.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'Metodo IInkAnalyzer:: SetDirtyRegion (IACom. h)'
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
ms.openlocfilehash: 72278dd9fe1d772d4ef340d25694d42f9c48ed7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129439"
---
# <a name="iinkanalyzersetdirtyregion-method"></a>Metodo IInkAnalyzer:: SetDirtyRegion

Modifica l'area che è stata modificata dopo l'ultima operazione di analisi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDirtyRegion* \[ in\]
</dt> <dd>

Oggetto [**IAnalysisRegion**](ianalysisregion.md) che descrive l'area modificata dall'ultima operazione di analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Questo metodo identifica le aree che devono essere analizzate o rianalizzate. Tutti i metodi [**IInkAnalyzer**](iinkanalyzer.md) che aggiungono, aggiornano o rimuovono i dati del tratto aggiornano l'area dirty. Per contrassegnare manualmente un'area per la rianalisi:

1.  Ottenere l'area dirty usando il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md).
2.  Usare il metodo [**IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md) o [**IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md) per aggiungere l'area all'area del passaggio 1.
3.  Usare il **Metodo IInkAnalyzer:: SetDirtyRegion** per aggiornare l'area dirty.

[**IInkAnalyzer**](iinkanalyzer.md) analizza l'input penna all'interno dell'area dirty durante una chiamata al metodo [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md). Tuttavia, **IInkAnalyzer** può espandere l'operazione di analisi per includere le aree adiacenti.

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

[**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




