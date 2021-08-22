---
description: Rimuove il tratto specificato da IInkAnalyzer.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: Metodo IInkAnalyzer::RemoveStroke (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd0a972ed776c40fc42d695df2058c62f9af84f8fc09155758d197772e9abfc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092011"
---
# <a name="iinkanalyzerremovestroke-method"></a>Metodo IInkAnalyzer::RemoveStroke

Rimuove il tratto specificato da [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*plStrokeId* \[ Pollici\]
</dt> <dd>

Identificatore del tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Questo metodo rimuove i dati del pacchetto per e fa riferimento al tratto specificato da [**IInkAnalyzer.**](iinkanalyzer.md)

Questo metodo rimuove il tratto dal nodo di contesto foglia che fa riferimento al tratto. Se [**IContextNode**](icontextnode.md) non fa più riferimento ad alcun tratto, questo metodo elimina gli oggetti **IContextNode** e i predecessori **IContextNode** che non hanno più nodi figlio.

Dopo che questo metodo rimuove il tratto da [**IContextNode,**](icontextnode.md)aggiorna l'area dirty dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il metodo [**IInkAnalyzer::GetDirtyRegion)**](iinkanalyzer-getdirtyregion.md)per includere il rettangolo di selezione del tratto rimosso.

Se *plStrokeId non* identifica un tratto associato a [**IInkAnalyzer,**](iinkanalyzer.md)questo metodo restituisce un risultato senza aggiornare l'analizzatore input penna.

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

[**Metodo IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




